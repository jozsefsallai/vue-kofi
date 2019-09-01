# vue-kofi

[![Build Status](https://travis-ci.org/jozsefsallai/vue-kofi.svg?branch=master)](https://travis-ci.org/jozsefsallai/vue-kofi)
[![NPM version](https://img.shields.io/npm/v/vue-kofi.svg?style=flat)](https://www.npmjs.com/package/vue-kofi)

Display Ko-fi widgets in your Vue components with ease.

## Installation

npm:

```
npm install vue-kofi --save
```

Yarn:

```
yarn add vue-kofi
```

Browser import:

```html
<script src="https://cdn.jsdelivr.net/npm/vue-kofi@1.1/dist/vue-kofi.js"></script>
```

## Usage

Import the component in your Vue mount script

```javascript
import Vue from 'vue';
import VueKofi from 'vue-kofi';

Vue.use(VueKofi);
// ...
```

Or, if you don't want to use it globally:

```javascript
import VueKofi from 'vue-kofi';
// ...
export default {
  // ...
  components: {
    VueKofi
  }
  // ...
};
```

Insert this into your template to display the button:

```html
<vue-kofi uid="YOUR_ID" />
```

## Props

| Name  | Type   | Required | Default               | Description                                                                       |
|-------|--------|----------|-----------------------|-----------------------------------------------------------------------------------|
| uid   | String | yes      | -                     | Your Ko-fi ID which you can get from your Ko-fi widget page. (e.g.: **A6251W51**) |
| color | String | no       | "#46b798"             | The background color of your Ko-fi button.                                        |
| text  | String | no       | "Support Me on Ko-fi" | The text that appears on the button.                                              |

---

*This is an open-source project and is not affiliated with or endorsed by Ko-fi.com*