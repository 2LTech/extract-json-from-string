[![Quality gate](https://sonarcloud.io/api/project_badges/quality_gate?project=2LTech_extract-json-from-string)](https://sonarcloud.io/summary/new_code?id=2LTech_extract-json-from-string)

** Forked from [tandrewnichols/extract-json-from-string](https://github.com/tandrewnichols/extract-json-from-string) **

# extract-json-from-string

Extract JSON/javascript objects from strings

## Installation

`npm install --save extract-json-from-string`

## Summary

Extract random JSON and javascript objects from a longer string, e.g. "Expected { foo: 'bar' } to equal { foo: 'baz' }". Also works with arrays.

## Usage

Just pass the string into the one exported function and get a list of objects and arrays contained therein returned to you. If the string contains no valid objects or arrays (**_valid_** objects or arrays), you'll get an empty array back.

### Node

```js
const extract = require('extract-json-from-string')

let objects = extract('Expected { foo: "bar" } to equal { foo: "baz" }')
// [
//   { foo: 'bar' },
//   { foo: 'baz' }
// ]
```

### Browser

```js
let objects = window.extractJson(
  'Expected { foo: "bar" } to equal { foo: "baz" }'
)
// [
//   { foo: 'bar' },
//   { foo: 'baz' }
// ]
```
