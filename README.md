# modulex

A module registration and load library

[![modulex](https://nodei.co/npm/modulex.png)](https://npmjs.org/package/modulex)
[![NPM downloads](http://img.shields.io/npm/dm/modulex.svg)](https://npmjs.org/package/modulex)
[![Build Status](https://secure.travis-ci.org/kissyteam/modulex.png?branch=master)](https://travis-ci.org/kissyteam/modulex)
[![Coverage Status](https://coveralls.io/repos/kissyteam/modulex/badge.png?branch=master)](https://coveralls.io/r/kissyteam/modulex?branch=master)
[![Dependency Status](https://gemnasium.com/kissyteam/modulex.png)](https://gemnasium.com/kissyteam/modulex)
[![Bower version](https://badge.fury.io/bo/modulex.svg)](http://badge.fury.io/bo/modulex)

[![browser support](https://ci.testling.com/kissyteam/modulex.png)](https://ci.testling.com/kissyteam/modulex)


## api

http://docs.kissyui.com/5.0/api/classes/Loader.html

### config environment

```javascript
modulex.config({
    packages: {},
    modules: {}
});
```

### register module

#### commonjs style

```javascript
modulex.add(function(require,exports,module){
});
```

or use define function

``` javascript
var define = modulex.add;
define(function(require,exports,module){
});
```

#### amd style

```javascript
modulex.add(function(X){
},{
    requires:['x']
});
```

### use module

can also load requirejs commonjs style module

```javascript
var require = modulex.use;
require(['x','u'],function(X,U){
});
```

## guide

http://docs.kissyui.com/5.0/guides/loader/index.html

## contribution

### prepare development environment

* npm install
* npm install -g gulp
* gulp server

### modify code

* modify source file inside lib

### run test cases

* open [http://localhost:8000/tests/runner.html](http://localhost:8000/tests/runner.html) to test
* open [http://localhost:8000/node_modules/node-jscover/lib/front-end/jscoverage.html?w=http://localhost:8000/tests/runner.html?coverage](http://localhost:8000/node_modules/node-jscover/lib/front-end/jscoverage.html?w=http://localhost:8000/tests/runner.html?coverage) to check test coverage

### pull request

* file an issue: [https://github.com/kissyteam/modulex/issues/new](https://github.com/kissyteam/modulex/issues/new)
* then pull request
