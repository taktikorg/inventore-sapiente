# @taktikorg/inventore-sapiente <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Is this value a JS Map? This module works cross-realm/iframe, and despite ES6 @@toStringTag.

## Example

```js
var isMap = require('@taktikorg/inventore-sapiente');
assert(!isMap(function () {}));
assert(!isMap(null));
assert(!isMap(function* () { yield 42; return Infinity; });
assert(!isMap(Symbol('foo')));
assert(!isMap(1n));
assert(!isMap(Object(1n)));

assert(!isMap(new Set()));
assert(!isMap(new WeakSet()));
assert(!isMap(new WeakMap()));

assert(isMap(new Map()));

class MyMap extends Map {}
assert(isMap(new MyMap()));
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@taktikorg/inventore-sapiente
[npm-version-svg]: https://versionbadg.es/inspect-js/@taktikorg/inventore-sapiente.svg
[deps-svg]: https://david-dm.org/inspect-js/@taktikorg/inventore-sapiente.svg
[deps-url]: https://david-dm.org/inspect-js/@taktikorg/inventore-sapiente
[dev-deps-svg]: https://david-dm.org/inspect-js/@taktikorg/inventore-sapiente/dev-status.svg
[dev-deps-url]: https://david-dm.org/inspect-js/@taktikorg/inventore-sapiente#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@taktikorg/inventore-sapiente.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@taktikorg/inventore-sapiente.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@taktikorg/inventore-sapiente.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@taktikorg/inventore-sapiente
[codecov-image]: https://codecov.io/gh/inspect-js/@taktikorg/inventore-sapiente/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/inspect-js/@taktikorg/inventore-sapiente/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/inspect-js/@taktikorg/inventore-sapiente
[actions-url]: https://github.com/taktikorg/inventore-sapiente/actions
