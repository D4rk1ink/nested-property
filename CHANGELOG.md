# CHANGELOG


### 4.0.0 - 30 SEP 2020

* Add type definitions for typescript projects. Note that this is the loosest definition possible to allow
typescript projects to compile without errors. Also embeds some useful documentation

### 3.0.0 - 27 SEP 2020

* Prevent mutation of Object.prototype to address a security issue: https://hackerone.com/reports/788883

### 2.0.2 - 22 AUG 2020

* Upgrade dependencies to fix vulnerabilites reported by dependa bot

### 2.0.0 - 18 FEB 2020

* Official 2.0.0 release, removing the `-beta1` version
* Extract CHANGELOG into a separate file as per #13

### 2.0.0-beta1 - 02 FEB 2020

* Add array wildcard `+` to access all properties nested within an array. For example:

```js
// sets all `name` property in the array to "<redacted>"
nestedProperty.set(array, "+.name", "<redacted>"); 
```

Closes [Issue #8](https://github.com/cosmosio/nested-property/issues/8). Thanks [vemuez](https://github.com/vemuez) for the suggestion!

### 2.0.1 - 23 JUNE 2020

* Upgrading dev dependencies to fix npm audit issues

### 2.0.0 - 18 FEB 2020

* Add support for array wildcards
* Add support for older browsers using babel

### 1.0.4 - 18 JAN 2020

* Fix license field in package.json. Thanks [zr87](https://github.com/zr87) for raising the issue!

### 1.0.3 - 15 JAN 2020

* replaced usage of `const` with `var` to maintain support of pre-ES6 JS interpreters. Thanks [stefanorie](https://github.com/stefanorie) for the contribution!

### 1.0.2 - 20 NOV 2019

* Update package-lock and remove yarn.lock to remove security alerts on dependencies

### 1.0.1 - 22 JUNE 2019

* Update to mocha 6.4.1 to remove security alerts on dependencies

### 1.0.0 - 22 JUNE 2019

* Breaking Change: When calling `set()` with an integer in the path and `nested-property` creates an object at the location, the object is now an array instead of an object. Hopefully, no user of the `nested-property` package should have been expecting to see an object instead of an array, but this constitutes a breaking changes, hence the major update in the semver.

Thanks [igor-barbosa](https://github.com/igor-barbosa) for the suggestion: [PR #2](https://github.com/cosmosio/nested-property/pull/2)

### 0.0.7 - 09 AUG 2016

* [Remove unused require('assert')](https://github.com/cosmosio/nested-property/pull/1), thanks to [Nilz11](https://github.com/Nilz11)

### 0.0.6 - 01 MAR 2015

* Fix a bug where an invalid path to search an object into is invalid and the isInNestedProperty would throw an error instead of return false

### 0.0.5 - 19 JAN 2015

* Add isIn, to tell if an object is on the path to a nested property.

### 0.0.4 - 15 JAN 2015

* Add {own: true} option to .has to ensure that a nested property isn't coming from the prototype chain
* Add hasOwn, that calls .has with the {own: true} option

### 0.0.3 - 14 JAN 2015

* Add has with tests and documentation
