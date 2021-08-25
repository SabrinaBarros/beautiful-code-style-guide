# JavaScript code style guide 🦜👩🏻‍💻👘📔

![keyboard](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/rkwepwglhcixd3j2gny2.gif)

## Summary 📑

- [Soft tabs with two spaces](#soft-tabs-with-two-spaces)
- [Never use semicolons](#never-use-semicolons)
- [Always use single quotes](#always-use-single-quotes)
- [Keep `else` in the same line of closure of the `if`](#keep-else-in-the-same-line-of-closure-of-the-if)
- [Add spaces between operators](#add-spaces-between-operators)
- [Avoid single letter names](#avoid-single-letter-names)
- [Use lowerCamelCase](#use-lowercamelcase)
- [Use the === operator](#use-the-===-operator)
- [Add spaces outside parentheses `()` but avoid it inside](#add-spaces-outside-parentheses-()-but-avoid-it-inside)
- [Use function expressions instead of function declarations](#use-function-expressions-instead-of-function-declarations)
- [Anonimous function](#when-you-must-use-function-expressions-(as-when-passing-an-anonymous-function),-use-arrow-function-notation)
- [Ternary operator](#ternary-operator)
- [Use `const` for all of your references, avoid using `var`](#use-const-for-all-of-your-references-avoid-using-var)
- [If you must reassign references, use `let` instead of `var`](#if-you-must-reassign-references-use-let-instead-of-var)
- [Declare one `const` or `let` per declaration statement](#declare-one-const-or-let-per-declaration-statement)
- [Use the literal syntax for `object` creation](#use-the-literal-syntax-for-object-creation)
- [Use the literal syntax for `array` creation](#use-the-literal-syntax-for-array-creation)
- [Declare `array` items in list](#declare-array-items-in-list)
- [Parentheses `()` and commas , are not followed by indented children on new lines](#parentheses-()-and-commas-`-are-not-followed-by-indented-children-on-new-lines)
- [Method chaining](#method-chaining)
- [Any non-trivial conditions must be assigned to a variable or function with a descriptive name](#any-non-trivial-conditions-must-be-assigned-to-a-variable-or-function-with-a-descriptive-name)
- [Try to write comments that explain higher level mechanisms or clarify difficult segments of your code](#try-to-write-comments-that-explain-higher-level-mechanisms-or-clarify-difficult-segments-of-your-code)
- [Don't use comments to trivial things](#dont-use-comments-to-trivial-things)
- [References](#references)

## Soft tabs with two spaces

*Eslint: [space-in-parens](https://eslint.org/docs/rules/space-in-parens)*

- Wrong:

```js
if (true) {
    console.log('True')
}
```

- Correct:

```js
if (true) {
  console.log('True')
}
```

## Never use semicolons

*Eslint: [semi](https://eslint.org/docs/rules/semi)*

- Wrong:

```js
if (true) {
  console.log('True');
}
```

- Correct:

```js
if (true) {
  console.log('True')
}
```

## Always use single quotes

*Eslint: [quotes](https://eslint.org/docs/rules/quotes)*

- Wrong:

```js
if (true) {
  console.log("True")
}
```
- Correct:

```js
if (true) {
  console.log('True')
}
```

## Keep `else` in the same line of closure of the `if`

*Eslint: [brace-style](https://eslint.org/docs/2.0.0/rules/brace-style)*

- Wrong:

```js
if (true) {
  console.log('True')
}
else {
  console.log('False')
}
```

- Correct:

```js
if (true) {
  console.log('True')
} else {
  console.log('False')
}
```

## Add spaces between operators

*Eslint: [space-infix-ops](https://eslint.org/docs/rules/space-infix-ops)*

- Wrong:

```js
for (i=0;i<10;i++) {
  ...
}
```

- Correct:

```js
for (i = 0; i < 10; i++) {
  ...
}
```

## Avoid single letter names

*Be descriptive with your naming. Eslint: [id-length](https://eslint.org/docs/rules/id-length)*

- Wrong:

```js
function q() {
  ...
}
```

- Correct:

```js
function query() {
  ...
}
```

## Use lowerCamelCase

*Eslint: [camelcase](https://eslint.org/docs/rules/camelcase)*

- Wrong:

```js
let is_error
```

- Correct:

```js
let isError
```

## Use the === operator

*Eslint: [eqeqeq](https://eslint.org/docs/rules/eqeqeq)*

- Wrong:

```js
const example = 'Is a example'

if (example == 15) {
  ...
}
```

- Correct:

```js
const example = 'Is a example'

if (example === 15) {
  ...
}
```

## Add spaces outside parentheses `()` but avoid it inside

*Eslint: [keyword-spacing](https://eslint.org/docs/rules/keyword-spacing)*

- Wrong:

```js
if(condition){
  ...
}
```

- Correct:

```js
if (condition) {
  ...
}
```

## Use function expressions instead of function declarations

*Eslint: [func-style](https://eslint.org/docs/rules/func-style)*

- Wrong:

```js
function foo() {
}
```

- Correct:

```js
const foo = function () { }
```

## When you must use function expressions (as when passing an anonymous function), use `arrow function` notation

*Eslint: [func-style](https://eslint.org/docs/rules/func-style)*

- Wrong:

```js
[1, 2, 3].map(function (x) {
  const y = x + 1
  return x * y
})
```

- Correct:

```js
[1, 2, 3].map((x) => {
  const y = x + 1
  return x * y
})
```

## Ternary operator

*The ternary operator should be used on a single line. Split it up into multiple lines instead. Eslint: [no-nested-ternay](https://eslint.org/docs/rules/no-nested-ternary)*

- Wrong:

```js
const foo = (condition)
  ? 1
  : 2
```

- Correct:

```js
const foo = (condition) ? 1 : 2
```

## Use `const` for all of your references, avoid using `var`

*Eslint: [no-var](https://eslint.org/docs/rules/no-var)*

- Wrong:

```js
var foo = 'bar'
```

- Correct:

```js
const foo = 'bar'
```

## If you must reassign references, use `let` instead of `var`

*Eslint: [no-var](https://eslint.org/docs/rules/no-var)*

- Wrong:

```js
var count = 1

if (condition) {
  count += 1
}
```

- Correct:

```js
let count = 'bar'

if (condition) {
  count += 1
}
```

## Declare one `const` or `let` per declaration statement

*Eslint: [one-var](https://eslint.org/docs/rules/one-var)*

- Wrong:

```js
const foo = require('./bar'),
      foo = require('./foo')
```

- Correct:

```js
const foo = require('./bar')
const foo = require('./foo')
```

## Use the literal syntax for `object` creation

*Eslint: [no-new-object](https://eslint.org/docs/rules/no-new-object)*

- Wrong:

```js
const foo = new Object()
```

- Correct:

```js
const foo = {}
```

## Use the literal syntax for `array` creation

*Eslint: [no-array-constructuor](https://eslint.org/docs/rules/no-array-constructor)*

- Wrong:

```js
const foo = new Array()
```

- Correct:

```js
const foo = []
```

## Declare `array` items in list

*Eslint: [array-element-newline](https://eslint.org/docs/rules/array-element-newline)*

- Wrong:

```js
const foo = [
  'hello', 'world'
]
```

```js
const foo = ['hello', 'world']
```

- Correct:

```js
const foo = [
  'hello',
  'word',
]
```

## Parentheses `()` and commas `,` are not followed by indented children on new lines

*Eslint: [function-paren-newline](https://eslint.org/docs/rules/function-paren-newline)*

- Wrong:

```js
foo.bar(
  'string',
  () => {
    statements
  }
)
```
- Correct:

```js
foo.bar('string', () => {
  statements
})
```

## Method chaining

*Eslint: [newline-per-chianed-call](https://eslint.org/docs/rules/newline-per-chained-call)*

- Wrong:

```js
user
.findOne({ name: 'foo' })
.populate('bar')
.exec(function(err, user) {
  return true
})
```

```js
user.findOne({ name: 'foo' })
  .populate('bar')
  .exec(function(err, user) {
    return true
  })
```

- Correct:

```js
user
  .findOne({ name: 'foo' })
  .populate('bar')
  .exec(function(err, user) {
    return true
  })
```

## Any non-trivial conditions must be assigned to a variable or function with a descriptive name

- Wrong:

```js
if (password.length >= 4 && /^(?=.*\d).{4,}$/.test(password)) {
  ...
}
```

- Correct:

```js
const isValidPassword = password.length >= 4 && /^(?=.*\d).{4,}$/.test(password)

if (isValidPassword) {
  ...
}
```

## Try to write comments that explain higher level mechanisms or clarify difficult segments of your code

- Wrong:

```js
const foo = "var(--bar)"

// Regexp
if (foo.replace(/var\(/, "").replace(/\)/, "") === "--bar") {
  ...
}
```

- Correct:

```js
let foo = 'var(--bar)'

let value = foo
            .replace(/var\(/, '') // Remove the 'var('
            .replace(/\)/, '') // Remove the ')'

if (foo === '--bar') {
  ...
}
```

## Don't use comments to trivial things

- Wrong:
```js

// Create the passwors
const password = 'carls1234'
```

- Correct:

```js
const password = 'carls1234'
```

## References

Project inspired by [valle-style-guide](https://github.com/valleweb/valle-style-guide/blob/master/js-style-guide.md)