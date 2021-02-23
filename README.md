<div align="center">
  <img src="/static/puzzle_logo.png" width="128px">
  <h1>Puzzle Pattern</h1>
</div>

<p align="center">
  Puzzle Pattern is a Vue.js development pattern created for code organization, while using the best practices, clean code, and much more.
</p>

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/guastallaigor/hare/master/LICENSE)

## Why use Puzzle Pattern?

When you are working with several different developers in one single project, the code tends to variate a lot one file to the other.

[ESLint](https://eslint.org/) usually helps us with that already. However, there are a lot of cases some linters may look the other way, when it shouldn't.

If you wish to maintain a code pattern throughout your entire project, with clean and organized code, that can also help with code maintenance, **this is the pattern for you!**

<a name="1"></a>

## [1](#1) MUST

<a name="1.1"></a>

- [1.1](#1.1) Use ES6 in full capacity;
  <a name="1.2"></a>
- [1.2](#1.2) Set a default language to be used throughout the project. If it's not your native language, define all the words will not be translated;
  <a name="1.3"></a>
- [1.3](#1.3) Define a code order inside your `<script>` that must be followed throughout all components. Only declare it if you are going to use it in your component. The recommended order is:

```javascript
// imports
export default {
  name: "",
  props: {},
  components: {},
  mixins: [],
  directives: {},
  data: () => ({}),
  computed: {},
  filters: {},
  beforeCreate() {},
  created() {},
  beforeMount() {},
  mounted() {},
  beforeUpdate() {},
  updated() {},
  beforeDestroy() {},
  destroyed() {},
  methods: {},
  watch: {},
};
```

<a name="1.4"></a>

- [1.4](#1.4) Props must always be an object with a declared type;
  <a name="1.5"></a>
- [1.5](#1.5) Props should be declared with lower `camelCase`. However, in the HTML they must be called with `kebab-case`;
  <a name="1.6"></a>
- [1.6](#1.6) Pass a parameter method only when needed;
  <a name="1.7"></a>
- [1.7](#1.7) Prioritize the use of `const`, otherwise use `let`;
  <a name="1.8"></a>
- [1.8](#1.8) The `data ()` declaration must be like this: `data: () => ({});` or `data: vm => ({});` when you need to use a Vue instance property.
  <a name="1.9"></a>
- [1.9](#1.9) If you wish to use the queryString when sending a GET request, use the `{ params }` object;
  <a name="1.10"></a>
- [1.10](#1.10) The `export default` must be at the same level of indentation as the `<script>`. The same goes for the first CSS property inside the `<style>`;
  <a name="1.11"></a>
- [1.11](#1.11) Remove all unused declarations, `vars` and empty tags. The same goes for the `<script>` and `<style>`;
  <a name="1.12"></a>
- [1.12](#1.12) One line break after all the `imports`;
  <a name="1.13"></a>
- [1.13](#1.13) One space always before and after a variable inside an interpolation;
  <a name="1.14"></a>
- [1.14](#1.14) Double quotes in all HTML tag attributes;
  <a name="1.15"></a>
- [1.15](#1.15) When a tag has more than one attribute, for each attribute place a line break;
  <a name="1.16"></a>
- [1.16](#1.16) Put a line break after each dot inside your script whenever possible;
  <a name="1.17"></a>
- [1.17](#1.17) When calling a method inside your HTML component, always put the parentheses "()";
  <a name="1.18"></a>
- [1.18](#1.18) Only use `mapGetters` when you are manipulating the `state`;
  <a name="1.19"></a>
- [1.19](#1.19) Moderate use of [vuex](https://github.com/vuejs/vuex), only in cases when you need the same state in a few components;
  <a name="1.20"></a>
- [1.20](#1.20) Using [vuex](https://github.com/vuejs/vuex), always use `mapGetters`, `mapState`, `mapActions` and `mapMutations`, instead of `this.$store`;
  <a name="1.21"></a>
- [1.21](#1.21) A [vuex's](https://github.com/vuejs/vuex) action should always return a promise.
  <a name="1.22"></a>
- [1.22](#1.22) `HTML` tags must have their declaration in the following order: Tag, id, class, attributes.
  <a name="1.23"></a>
- [1.23](#1.23) `Destructuring assignment` should be only for variables and never for methods. Example: `let { girls, guys, women, men } = state`.
  <a name="1.24"></a>
- [1.24](#1.24) Component files must have upper `camel Case` name (**except** in `index.vue` files).

<a name="2"></a>

## [2](#2) SHOULD

<a name="2.1"></a>

- [2.1](#2.1) Use `computed properties` in your HTML instead of methods;
  <a name="2.2"></a>
- [2.2](#2.2) Use `filter`, `map`, `reduce` and `find`;
  <a name="2.3"></a>
- [2.3](#2.3) Create customized events rather than props with type Function which returns a callback;
  <a name="2.4"></a>
- [2.4](#2.4) Use the `created ()` _Lifecycle_ rather than `mounted ()`;
  <a name="2.5"></a>
- [2.5](#2.5) Use `v-if` instead of `v-show`;
  <a name="2.6"></a>
- [2.6](#2.6) Use the `.sync` modifier rather than `v-model`;
  <a name="2.7"></a>
- [2.7](#2.7) Use display flex rather than other types of display;
  <a name="2.8"></a>
- [2.8](#2.8) Import your files with "@" rather than "../";
  <a name="2.9"></a>
- [2.9](#2.9) Whenever you are going to duplicate a code, create a mixin instead and declare it locally.

<a name="3"></a>

## [3](#3) AVOID

<a name="3.1"></a>

- [3.1](#3.1) Using watchs, use computed instead;
  <a name="3.2"></a>
- [3.2](#3.2) Using `var`, use `const` or `let` instead;
  <a name="3.3"></a>
- [3.3](#3.3) Using `else`, prioritize early return;
  <a name="3.4"></a>
- [3.4](#3.4) Using `switch case`;
  <a name="3.5"></a>
- [3.5](#3.5) Using `forEach`, `for in`, `for` and `while`;
  <a name="3.6"></a>
- [3.6](#3.6) Using the attribute `style` static in your HTML tags;
  <a name="3.7"></a>
- [3.7](#3.7) Using `scoped` on your `<style>`, instead create a class and wrap all your `<template>` on it, then put all other class you have inside that one;
  <a name="3.8"></a>
- [3.8](#3.8) Using the `beforeUpdate ()` and `updated ()` _Lifecycle_;
  <a name="3.9"></a>
- [3.9](#3.9) Using the directive `v-html`;
  <a name="3.10"></a>
- [3.10](#3.10) Using more than one props type;
  <a name="3.11"></a>
- [3.11](#3.11) Declaring global filters;
  <a name="3.12"></a>
- [3.12](#3.12) Declaring global directives;
  <a name="3.13"></a>
- [3.13](#3.13) Declaring global components with `Vue.component()`;
  <a name="3.14"></a>
- [3.14](#3.14) Treating Date as a String, use [momentjs](https://momentjs.com/) instead;
  <a name="3.15"></a>
- [3.15](#3.15) Having several levels of indentation;
  <a name="3.16"></a>
- [3.16](#3.16) In a request, avoid grabbing all of the `response`. Instead, grab only what you are going to actually use.

<a name="4"></a>

## [4](#4) DON'T

<a name="4.1"></a>

- [4.1](#4.1) Declare global mixins;
  <a name="4.2"></a>
- [4.2](#4.2) Use the `v-bind` directive. Instead, use the short term (:);
  <a name="4.3"></a>
- [4.3](#4.3) Use the `v-on` directive. Instead, use the short term (@);
  <a name="4.4"></a>
- [4.4](#4.4) Use a `div` as an actual `div` using [Pug](https://github.com/pugjs/pug). Create a class or id instead;
  <a name="4.5"></a>
- [4.5](#4.5) Use `style`, `height`, `width`, and other **static** attribute tags inside them directly. Create a class instead;
  <a name="4.6"></a>
- [4.6](#4.6) Use [jQuery](https://jquery.com/).

### Code Style Recommended

This is the code style that was used to create this pattern and it's recommended to use Puzzle Pattern in it's full potential.

[![js-standard-style](https://cdn.rawgit.com/feross/standard/master/badge.svg)](https://github.com/feross/standard)

### Template Engine Recommended

[Pug](https://github.com/pugjs/pug) is highly recommended to use in all your `<template>` thorough your project.

### TODO

- [ ] Add code examples.
- [ ] Develop a Puzzle ESLint.
- [ ] Develop a Puzzle Editor Plugin.

## Contributors

<div style="display:flex;flex-flow:row wrap;align-items:center">
  <a href="https://github.com/guastallaigor">
    <img
      align="center"
      src="/static/contributor_1.png"
      width="100px"
      height="100px"
      style="padding-right:10px"
      alt="guastallaigor">
  </a>
  <a href="https://github.com/iliojunior">
    <img
      align="center"
      src="/static/contributor_2.png"
      width="100px"
      height="100px"
      alt="iliojunior">
  </a>
  <a href="https://github.com/EduardoDrozda">
    <img
      align="center"
      src="/static/contributor_3.png"
      width="100px"
      height="100px"
      alt="EduardoDrozda">
  </a>
</div>

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/C1C63QCB8)

## License

MIT © [guastallaigor](https://github.com/guastallaigor/puzzle-pattern)
