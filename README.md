<div align="center">
  <img src="static/logo.png" width="128px">
  <h1>Puzzle Pattern</h1>
</div>

<p align="center">
  Puzzle Pattern is a VueJS development pattern created for code organization, using the best practices, clean code, and much more.
</p>

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/guastallaigor/hare/master/LICENSE)

## Why use the Puzzle Pattern?

## MUST

* Use ES6 in full capacity;
* Set a default language to be used throughout the project. If it's not your native language, set all the words will not be translated;
* Define a code order inside your `<script>` that must be followed throughout all components. Only declare it if you are going to use it in your component. The recommended order is:
  1. `imports`;
  2. `export default {}`;
  3. `props: {}`;
  4. `components: {}`;
  5. `mixins: []`;
  6. `directives: {}`;
  7. `data: () => ({})`;
  8. `computed: {}`;
  9. `filters: {}`;
  10. `beforeCreate () {}`;
  11. `created () {}`;
  12. `beforeMount () {}`;
  13. `mounted () {}`;
  14. `beforeUpdate () {}`;
  15. `updated () {}`;
  16. `beforeDestroy () {}`;
  17. `destroyed () {}`;
  18. `methods () {}`;
  19. `watch: () {}`;
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
* Only use mapGetters when you are manipulating the state;
* Moderate use of [vuex](https://github.com/vuejs/vuex), only in cases when you need the same state in a few components;
* Using [vuex](https://github.com/vuejs/vuex), always use mapGetters, mapState, mapActions and mapMutations, instead of this.$store;

## SHOULD

## AVOID

## DON'T

#### Code Style Recommended

This is the code style that was used to create this pattern.

[![js-standard-style](https://cdn.rawgit.com/feross/standard/master/badge.svg)](https://github.com/feross/standard)

### TODO

* [ ] Create a Puzzle ESLint.

## License

MIT © [guastallaigor](https://github.com/guastallaigor/puzzle-pattern)
