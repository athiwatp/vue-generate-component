# Vue js component generator [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

CLI util for easy generate Vue js component
## Installation
```js
npm install -g vue-generate-component
```

## Usage

```bash
vgc --help
```

####**Create new component**####
```bash
vgc footer
```
Will generate four files:

**footer.component.js**
```javascript
export default  {
  name: 'footer',
  props: [],
  mounted() {
    
  },
  data() {
    return {
      
    }
  },
  methods: {
   
  },
  computed: {

  }
}

```

**footer.component.spec.js**
```javascript
import Vue from 'vue';
import FooterComponent from './index.vue';

// Here are some Jasmine 2.0 tests, though you can
// use any test runner / assertion library combo you prefer
describe('FooterComponent', () => {
  // Inspect the raw component options
  it('has a created hook', () => {
    // expect(typeof FooterComponent.created).toBe('function');
  })
  // Evaluate the results of functions in
  // the raw component options
  it('sets the correct default data', () => {
    // expect(typeof FooterComponent.data).toBe('function')
    // const defaultData = FooterComponent.data();
    // expect(defaultData.message).toBe('hello!');
  })
  // Inspect the component instance on mount
  it('correctly sets the message when created', () => {
    // const vm = new Vue(FooterComponent).$mount();
    // expect(vm.message).toBe('bye!');
  })
  // Mount an instance and inspect the render output
  it('renders the correct message', () => {
    // const Ctor = Vue.extend(FooterComponent);
    // const vm = new Ctor().$mount();
    // expect(vm.$el.textContent).toBe('bye!');
  })
})

```

**footer.component.html**
```html
<section class="footer">
  <h1>footer Component</h1>
</section>

```

**footer.component.scss**
```css
.footer {

}
```

####**Create new component single file**####
```bash
vgc -s home
```
will generate one vue file:
```javascript
<template lang="html">
  <section class="home">
    <h1>home Component</h1>
  </section>
</template>

<script lang="js">
  export default  {
    name: 'home',
    props: [],
    mounted() {
      
    },
    data() {
      return {
        
      }
    },
    methods: {
    
    },
    computed: {

    }
}
</script>

<style scoped lang="scss">
  .home {

  }
</style>
```

####**Create new component single file inside new folder**####
```bash
vgc -s home --folder
```

####**Create new directive**####
```bash
vgc -d my-directive
```
will generate:

**my-directive.directive.js**
```javascript
import Vue from 'vue';

Vue.directive('my-directive', {
  bind() {

  },
  // When the bound element is inserted into the DOM...
  inserted(el) {
    // el.focus();
  },
  update() {

  },
  unbind() {

  }
})
```

### Change the default file types for html and style
If you are using something else from the default html and scss you can set this one time like this:
```bash
sudo vgc --html jade --style less
```
### PR ME!!!
If you want to fix/improve the templates please PR ME.
