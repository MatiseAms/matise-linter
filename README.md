# Matise linter
Before using our settings be sure to follow our instruction.


### Atom Requirements
** Atom packages **
* linter-eslint
* prettier-atom
* language-vue

** linter-eslint settings **
* Fix errors on save: `enabled` | `disabled` (optional)
* List of scopes to run ESLint on, run 'Editor: Log': add value `text.html.vue` (required)
* Show Rule ID in Messages: `enabled`(required)
* Use global ESLint installation: `Disabled` (required)

** prettier-atom settings **
* ESLint Integration: `enabled` (required)
* Format Files on Save: `enabled` | `disabled` (optional)

### VSCode Requirements
** VSCode packages **

* Prettier - Code formatter
* ESlint
* Vetur

To use Vue for ESlint you have to ue the Vue settings

`"eslint.validate": [ "javascript", "javascriptreact", "vue" ]`

VSCode has some issues following the autosave of prettier and the ESLint config. If you know how to fix this problem please create a PR.

### NPM Requirements

To use the config you have to install the following NPM packages:

```
"eslint": "^5.6.0",
"eslint-config-prettier": "^3.1.0",
"eslint-friendly-formatter": "^4.0.1",
"eslint-loader": "^2.1.1",
"eslint-plugin-prettier": "^2.7.0",
"eslint-plugin-vue": "^4.7.1"
```


## Linter Options
I'll list some options that are opinionated. All other options are an combination of the Vue standard and ESlint standard. Our parser is Babal-eslint

#### vue/no-dupe-keys
Results in an error. No duplicate use of keys can be used.

[Docs and examples](https://github.com/vuejs/eslint-plugin-vue/blob/master/docs/rules/no-dupe-keys.md)

#### vue/no-duplicate-attributes
Results in an warning. No duplicate use of attributes in Vue. If you want to use multiple attributes you can use the bind option of Vue.

[Docs and examples](https://github.com/vuejs/eslint-plugin-vue/blob/master/docs/rules/no-duplicate-attributes.md)

#### vue/no-reserved-keys
Results in an error. These keys are reserved by Vue. Overriding these settings results in an error.

[Docs and examples](https://github.com/vuejs/eslint-plugin-vue/blob/master/docs/rules/no-reserved-keys.md)

#### no-side-effects-in-computed-properties
Results in an error. You can't manipulate computed properties.  

[Docs and examples](https://github.com/vuejs/eslint-plugin-vue/blob/master/docs/rules/no-side-effects-in-computed-properties.md)

#### no-template-key
Results in an error. You can't use the `key` attribute on a template.

[Docs and examples](https://github.com/vuejs/eslint-plugin-vue/blob/master/docs/rules/no-template-key.md)

#### html-closing-bracket-newline
Results in an warning. For singleline components you can't use a linebreak to close the element. For multiline components you have to use a linebreak to close the element.

[Docs and examples](https://github.com/vuejs/eslint-plugin-vue/blob/master/docs/rules/html-closing-bracket-newline.md)

#### html-closing-bracket-spacing
Results in an warning.
* startTag: `never`
* endTag: `never`
* selfClosingTag: `always`

[Docs and examples](https://github.com/vuejs/eslint-plugin-vue/blob/master/docs/rules/html-closing-bracket-spacing.md)

#### html-self-closing
Results in an warning.
* void: `always`
* normal: `always`
* component: `always`

[Docs and examples](https://github.com/vuejs/eslint-plugin-vue/blob/master/docs/rules/html-self-closing.md)

#### max-attributes-per-line
Results in an warning. We use a maxiumum of 3 attributes for an element. Multiline has a max of 1.

[Docs and examples](https://github.com/vuejs/eslint-plugin-vue/blob/master/docs/rules/max-attributes-per-line.md)

#### mustache-interpolation-spacing
Results in an warning. We use a space for adding a Vue elements into the DOM.

[Docs and examples](https://github.com/vuejs/eslint-plugin-vue/blob/master/docs/rules/mustache-interpolation-spacing.md)

#### this-in-template
Results in an error. Don't use `this` in the template

[Docs and examples](https://github.com/vuejs/eslint-plugin-vue/blob/master/docs/rules/this-in-template.md)


## Final
These settings are opinionated, please read them carefully, even the `.eslintrc.js`. If you find something please create a PR or an issue on this repo.

## Sources

* [https://github.com/vuejs/eslint-plugin-vue](https://github.com/vuejs/eslint-plugin-vue)
* [https://prettier.io/docs/en/eslint.html](https://prettier.io/docs/en/eslint.html)
* [https://eslint.org/docs/rules/](https://eslint.org/docs/rules/)
