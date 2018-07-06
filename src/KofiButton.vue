<template>
  <div class="btn-container">
    <a class="kofi-button" :href="kofiUrl" :style="styles" target="_blank" title="Support me on ko-fi.com">
      <span class="kofitext">
        <img class="kofiimg" src="./cup.svg" />
        {{ text }}
      </span>
    </a>
  </div>
</template>

<script>
  export default {
    name: 'vue-kofi',
    props: {
      uid: { type: String, required: true },
      color: { type: String, default: '#46b798' },
      text: { type: String, default: 'Support Me on Ko-fi' }
    },
    computed: {
      kofiUrl: function() {
        return `https://ko-fi.com/${this.uid}`;
      },
      styles: function() {
        return {
          'background-color': this.color
        };
      }
    }
  };
</script>

<style lang="scss" scoped>
  @import url('https://fonts.googleapis.com/css?family=Lato&subset=latin,latin-ext');
  
  .btn-container {
    display: inline-block;
    white-space: nowrap;
    min-width: 160px;

    .kofi-button {
      box-shadow: 1px 2px 1px rgba(0, 0, 0, 0.2);
      line-height: 32px;
      min-width: 150px;
      display: inline-block;
      background-color: #46b798;
      padding: 2px 11px;
      text-align: center;
      border-radius: 3px;
      color: #fff;
      cursor: pointer;
      overflow-wrap: break-word;
      vertical-align: middle;
      border: 0 none #fff;
      font-family: 'Lato', Helvetica, Century Gothic, sans-serif;
      text-decoration: none;
      text-shadow: none;
      font-weight: 400;
      font-size: 14px;
    }

    &:visited, &:hover, &:active {
      text-decoration: none;
    }

    &:visited {
      color: #fff;
    }

    &:hover {
      opacity: .85;
      color: #f5f5f5;
    }

    &:active {
      color: #f5f5f5;
    }

    .kofitext {
      color: #fff;
      letter-spacing: -0.15px;
      word-wrap: none;
      vertical-align: middle;
      line-height: 33px;
      padding: 0;
      text-align: center;
      text-decoration: none;
      text-shadow: 0 1px 1px rgba(34, 34, 34, 0.3);

      .kofiimg {
        display: initial;
        vertical-align: middle;
        height: 13px;
        width: 20px;
        padding-top: 0;
        padding-bottom: 0;
        border: none;
        margin-top: 0;
        margin-right: 5px;
        margin-left: 0;
        margin-bottom: 4px;
        content: url('./cup.svg');
        filter: drop-shadow(0 1px 1px rgba(34, 34, 34, 0.3));
        -webkit-filter: drop-shadow(0 1px 1px rgba(34, 34, 34, 0.3));

        &:after {
          vertical-align: middle;
          height: 25px;
          padding-top: 0;
          padding-bottom: 0;
          border: none;
          margin-top: 0;
          margin-right: 6px;
          margin-left: 0;
          margin-bottom: 4px;
          content: url('./white.svg');
        }
      }
    }
  }
</style>
