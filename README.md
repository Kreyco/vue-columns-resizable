# vue-columns-resizable-vuetify

<p>
  <a href="https://www.npmjs.com/package/vue-columns-resizable-vuetify"><img src="https://img.shields.io/npm/v/vue-columns-resizable-vuetify.svg" alt="Version"></a>
  <a href="https://www.npmjs.com/package/vue-columns-resizable-vuetify"><img src="https://img.shields.io/npm/dt/vue-columns-resizable-vuetify.svg" alt="Downloads"></a>
  <a href="https://www.npmjs.com/package/vue-columns-resizable-vuetify"><img src="https://img.shields.io/npm/l/vue-columns-resizable-vuetify.svg" alt="License"></a>
</p>

## Project based

https://github.com/Fuxy526/vue-columns-resizable
https://www.npmjs.com/package/vue-columns-resizable

And using Pull Request from
https://github.com/onmotion/vue-columns-resizable

## Changes

Allow use on top elements (Vuetify use)

## Setup
Vue directive for making table columns resizable.

[demo](https://fuxy526.github.io/vue-columns-resizable/)

![](preview.gif)

## Install

```sh
npm install vue-columns-resizable-vuetify --save
```

## Usage

#### main.js

```javascript
import VueColumnsResizableVuetify from './plugins/vue-columns-resizable-vuetify';

Vue.use(VueColumnsResizableVuetify);
```

#### *.vue

```html
<table border="1" class="table" v-columns-resizable>
  <thead>
    <tr>
      <th width="50%">name</th>
      <th width="25%">age</th>
      <th width="25%">gender</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>John</td>
      <td>20</td>
      <td>male</td>
    </tr>
    <tr>
      <td>Emma</td>
      <td>18</td>
      <td>female</td>
    </tr>
    <tr>
      <td>Peter</td>
      <td>21</td>
      <td>male</td>
    </tr>
  </tbody>
</table>
```

Resize on thead

```html
<table border="1" class="table">
  <thead v-columns-resizable>
    <tr>
      <th width="50%">name</th>
      <th width="25%">age</th>
      <th width="25%">gender</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>John</td>
      <td>20</td>
      <td>male</td>
    </tr>
    <tr>
      <td>Emma</td>
      <td>18</td>
      <td>female</td>
    </tr>
    <tr>
      <td>Peter</td>
      <td>21</td>
      <td>male</td>
    </tr>
  </tbody>
</table>
```

Resize on v-data-table (Using Vuetify ^2.0)

```html
<v-data-table
    ref="table"
    v-model="selected"
    v-columns-resizable
>
    <template v-slot:items="{ props }"> //It is not necessary to use template at all
    </template>
</v-data-table>
```


## Changelog

* 1.0.3 - Allow use on top elements (Vuetify use)
* 0.0.1 - Resize on columns & Resize on thead
