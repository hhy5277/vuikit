<p align="center">
  <a href="https://vuikit.github.io/vuikit">
    <img width="150" src="https://cdn.rawgit.com/vuikit/vuikit/master/static/logo-vuikit.svg">
  </a>
</p>

> UIkit with all the power of Vue

Vuikit is a collection of Vue components built on top of the awesome UIkit framework. While it is possible to use UIkit by its own when building Vue components, you may find yourself building a wrapper around it to fill the missing logic gap or to make it behave more naturally with Vue. Vuikit solves all that by providing a precise, documented API.

## Documentation and examples

There is a live demo at [http://vuikit.github.io/vuikit](http://vuikit.github.io/vuikit) with technical information about each component. As well as a [codepen](http://codepen.io/miljan/pen/YWXVKj) playground.

## Dependencies

- [Vue](http://vuejs.org/) (^2.0.0)
- [Moment](http://momentjs.com/) (^2.14.1) - Only required by VkCalendar

Yeah! Since Vuikit 0.6.0 the only general dependency is Vue!

## Code Samples
> Note that all code examples are using ES6 syntax

Vuikit components are registered globally by default and ready to be used immediately.

```js
import Vue from 'vue'
import Vuikit from 'vuikit'

Vue.use(Vuikit)
```
```html
<template>
  <div>
    <vk-button-checkbox>
      <vk-button color="primary">Button</vk-button>
      <vk-button active>Button</vk-button>
      <vk-button>Button</vk-button>
    </vk-button-checkbox>
  </div>
</template>
```

Although is possible to load and register them individually.

```js
import Vue from 'vue'
import { Button, Modal } from 'vuikit'

// globally
Vue.component('VkButton', Button)
Vue.component('VkModal', Modal)

// or locally
new Vue({
  components: {
    VkButton: Button,
    VkModal: Modal
  }
})
```

Changing the output or adding specific features is straightforward by extending a component.

```js
import Vue from 'vue'
import { Button } from 'vuikit'

Vue.component('TmButton', {
  extends: Button,
  template: '', // the new output
  props: {} // new features
  ...
})
```

## Configuration and Usage

### NPM

```bash
npm install vuikit --save
```
```js
import Vue from 'vue'
import Vuikit from 'vuikit'

Vue.use(Vuikit) // or register individually
```

### Browser

Make sure Vue is loaded upfront and then load `dist/vuikit.js`.

## Developers

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for distribution
npm run build
```

## License

Vuikit is open source and released under the [MIT License](LICENSE.md).

Copyright (c) 2016 ZOOlanders.com
