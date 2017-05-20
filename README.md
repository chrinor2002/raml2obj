# RAML to object

[![NPM version](http://img.shields.io/npm/v/raml2obj.svg)](https://www.npmjs.org/package/raml2obj)
[![Prettier](https://img.shields.io/badge/code%20style-prettier-blue.svg?style=flat)](https://github.com/prettier/prettier)

A thin wrapper around [raml-js-parser-2](https://github.com/raml-org/raml-js-parser-2), adding extra properties to the resulting
object for use in [raml2html](https://www.npmjs.org/package/raml2html) and [raml2md](https://www.npmjs.org/package/raml2md).

Versions 4.0.0 and up only support RAML 1.x files. If you still have RAML 0.8 source files, please stick with raml2obj 3.

## Install
```
npm i raml2obj --save
```


## Usage
```js
var raml2obj = require('raml2obj');

// source can either be a filename, url, or parsed RAML object.
// Returns a promise.
raml2obj.parse(source).then(function(ramlObj) {
  // Do something with the resulting ramlObj :)
});
```

## Usage With Options
```js
var raml2obj = require('raml2obj');

// source can either be a filename, url, or parsed RAML object.
// Returns a promise.
// Options are any parser options that is supported by raml-js-parser-2
var options = {};
raml2obj.parseWithOptions(source, options).then(function(ramlObj) {
  // Do something with the resulting ramlObj :)
});
```

## Contribute
raml2obj is an open source project and your contribution is very much appreciated.

1. Check for open issues or open a fresh issue to start a discussion around a feature idea or a bug.
2. Fork the repository on Github and make your changes on the **develop** branch (or branch off of it).
   Run `npm run lint` before committing to check for common problems and auto format all code.
3. Add unit tests, run them with `npm run test`
4. Send a pull request (with the develop branch as the target).

A big thank you goes out to everyone who helped with the project, the [contributors](https://github.com/raml2html/raml2obj/graphs/contributors)
and everyone who took the time to report issues and give feedback.


## License
raml2obj is available under the MIT license. See the LICENSE file for more info.
