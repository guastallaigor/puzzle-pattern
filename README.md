<div align="center">
  <img src="puzzle.png" width="128px">
  <h1>Puzzle Pattern</h1>
</div>

<p align="center">
  Puzzle Pattern is a VueJS development pattern created for code organization, using the best practices, clean code, and much more.
</p>

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/guastallaigor/hare/master/LICENSE)

## Why use the Puzzle Pattern?

...

## MUST

* Use ES6 in full capacity;
* Set a default language to be used throughout the project. If it's not your native language, define all the words will not be translated;
* Define a code order inside your `<script>` that must be followed throughout all components. Only declare it if you are going to use it in your component. The recommended order is:

      1.  imports
      2.  export default {
        2.1.  props: {}
        2.2.  components: {}
        2.3.  mixins: []
        2.4.  directives: {}
        2.5.  data: () => ({})
        2.6.  computed: {}
        2.7.  filters: {}
        2.8.  beforeCreate () {}
        2.9.  created () {}
        2.10.  beforeMount () {}
        2.11.  mounted () {}
        2.12.  beforeUpdate () {}
        2.13.  updated () {}
        2.14.  beforeDestroy () {}
        2.15.  destroyed () {}
        2.16.  methods () {}
        2.17.  watch: () {}
      }

* Props must always be an object with a declared type;
* Props should be declared with lower `camelCase`. However, in the HTML they must be called with `kebab-case`;
* Pass a parameter method only when needed;
* Prioritize the use of `const`, otherwise use `let`;
* The `data ()` declaration must be like this: `data: () => ({});`
* If you wish to use the queryString when sending a GET request, use the `{ params }` object;
* The `export default` must be at the same level of indentation as the `<script>`. The same goes for the first css property inside the `<style>`;
* Remove all unused declarations, `vars` and empty tags. The same goes for the `<script>` and `<style>`;
* One line break after all the `imports`;
* One space always before and after a variable inside an interpolation;
* Double quotes in all HTML tag attributes;
* When a tag has more than one attribute, put on a line break;
* Put a line break after each dot inside your script whenever possible;
* When calling a method inside your HTML component, always put the parentheses "()";
* Only use `mapGetters` when you are manipulating the `state`;
* Moderate use of [vuex](https://github.com/vuejs/vuex), only in cases when you need the same state in a few components;
* Using [vuex](https://github.com/vuejs/vuex), always use `mapGetters`, `mapState`, `mapActions` and `mapMutations`, instead of `this.$store`;

## SHOULD

## AVOID

## DON'T

#### Code Style Recommended

This is the code style that was used to create this pattern.

[![js-standard-style](https://cdn.rawgit.com/feross/standard/master/badge.svg)](https://github.com/feross/standard)

### TODO

* [ ] Write the "Why use the Puzzle Pattern?" section.
* [ ] Write the "Should" section.
* [ ] Write the "Avoid" section.
* [ ] Write the "Don't" section.
* [ ] Develop a Puzzle ESLint.
* [ ] Develop a Puzzle Editor Plugin.

## License

MIT © [guastallaigor](https://github.com/guastallaigor/puzzle-pattern)
