# npmdoc-node-cache

#### basic api documentation for  [node-cache (v4.1.1)](https://github.com/mpneuried/nodecache)  [![npm package](https://img.shields.io/npm/v/npmdoc-node-cache.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-node-cache) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-node-cache.svg)](https://travis-ci.org/npmdoc/node-npmdoc-node-cache)

#### Simple and fast NodeJS internal caching. Node internal in memory cache like memcached.

[![NPM](https://nodei.co/npm/node-cache.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/node-cache)

- [https://npmdoc.github.io/node-npmdoc-node-cache/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-node-cache/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-node-cache/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-node-cache/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-node-cache/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-node-cache/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "mpneuried"
    },
    "bugs": {
        "url": "https://github.com/mpneuried/nodecache/issues"
    },
    "dependencies": {
        "clone": "2.x",
        "lodash": "4.x"
    },
    "description": "Simple and fast NodeJS internal caching. Node internal in memory cache like memcached.",
    "devDependencies": {
        "coffee-coverage": "1.x",
        "coffee-script": "1.x",
        "coveralls": "2.x",
        "grunt": "0.4.x",
        "grunt-banner": "0.6.x",
        "grunt-contrib-clean": "1.0.x",
        "grunt-contrib-coffee": "1.0.x",
        "grunt-contrib-watch": "1.x",
        "grunt-include-replace": "3.2.x",
        "grunt-mocha-cli": "2.x",
        "grunt-regarde": "0.1.x",
        "grunt-run": "0.5.x",
        "istanbul": "0.x",
        "mocha": "3.x",
        "should": "11.x"
    },
    "directories": {},
    "dist": {
        "shasum": "08524645ee4039dedc3dcc1dd7c6b979e0619e44",
        "tarball": "https://registry.npmjs.org/node-cache/-/node-cache-4.1.1.tgz"
    },
    "engines": {
        "node": ">= 0.4.6"
    },
    "gitHead": "37ac785c68716b60cdfdbd52bc51cb60fadf8c79",
    "homepage": "https://github.com/mpneuried/nodecache",
    "keywords": [
        "cache",
        "caching",
        "local",
        "variable",
        "multi",
        "memory",
        "internal",
        "node",
        "memcached",
        "object"
    ],
    "license": "MIT",
    "main": "./index.js",
    "maintainers": [
        {
            "name": "tcs-de"
        }
    ],
    "name": "node-cache",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/mpneuried/nodecache.git"
    },
    "scripts": {
        "build": "grunt build",
        "test": "COFFEECOV_INIT_ALL=false mocha --compilers coffee:coffee-script/register --require coffee-coverage/register-istanbul _src/test/mocha_test.coffee -R spec",
        "test-docker": "SILIENT_MODE=1 mocha test/mocha_test.js -R min"
    },
    "tags": [
        "cache",
        "caching",
        "local",
        "variable",
        "multi",
        "memory",
        "internal",
        "node",
        "memcached",
        "object"
    ],
    "version": "4.1.1",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
