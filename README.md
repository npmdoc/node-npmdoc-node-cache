# api documentation for  [node-cache (v4.1.1)](https://github.com/mpneuried/nodecache)  [![npm package](https://img.shields.io/npm/v/npmdoc-node-cache.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-node-cache) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-node-cache.svg)](https://travis-ci.org/npmdoc/node-npmdoc-node-cache)
#### Simple and fast NodeJS internal caching. Node internal in memory cache like memcached.

[![NPM](https://nodei.co/npm/node-cache.png?downloads=true)](https://www.npmjs.com/package/node-cache)

[![apidoc](https://npmdoc.github.io/node-npmdoc-node-cache/build/screenCapture.buildNpmdoc.browser.%2Fhome%2Ftravis%2Fbuild%2Fnpmdoc%2Fnode-npmdoc-node-cache%2Ftmp%2Fbuild%2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-node-cache/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-node-cache/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-node-cache/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "mpneuried",
        "email": "mp@tcs.de"
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
            "name": "tcs-de",
            "email": "github@tcs.de"
        }
    ],
    "name": "node-cache",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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
    "version": "4.1.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module node-cache](#apidoc.module.node-cache)
1.  boolean <span class="apidocSignatureSpan">node-cache.</span>usingDomains
1.  [function <span class="apidocSignatureSpan">node-cache.</span>EventEmitter ()](#apidoc.element.node-cache.EventEmitter)
1.  [function <span class="apidocSignatureSpan">node-cache.</span>init ()](#apidoc.element.node-cache.init)
1.  [function <span class="apidocSignatureSpan">node-cache.</span>listenerCount (emitter, type)](#apidoc.element.node-cache.listenerCount)
1.  number <span class="apidocSignatureSpan">node-cache.</span>defaultMaxListeners
1.  object <span class="apidocSignatureSpan">node-cache.</span>__super__
1.  string <span class="apidocSignatureSpan">node-cache.</span>version



# <a name="apidoc.module.node-cache"></a>[module node-cache](#apidoc.module.node-cache)

#### <a name="apidoc.element.node-cache.EventEmitter"></a>[function <span class="apidocSignatureSpan">node-cache.</span>EventEmitter ()](#apidoc.element.node-cache.EventEmitter)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-cache.init"></a>[function <span class="apidocSignatureSpan">node-cache.</span>init ()](#apidoc.element.node-cache.init)
- description and source-code
```javascript
init = function () {
  this.domain = null;
  if (EventEmitter.usingDomains) {
    // if there is an active domain, then attach to it.
    domain = domain || require('domain');
    if (domain.active && !(this instanceof domain.Domain)) {
      this.domain = domain.active;
    }
  }

  if (!this._events || this._events === Object.getPrototypeOf(this)._events) {
    this._events = new EventHandlers();
    this._eventsCount = 0;
  }

  this._maxListeners = this._maxListeners || undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-cache.listenerCount"></a>[function <span class="apidocSignatureSpan">node-cache.</span>listenerCount (emitter, type)](#apidoc.element.node-cache.listenerCount)
- description and source-code
```javascript
listenerCount = function (emitter, type) {
  if (typeof emitter.listenerCount === 'function') {
    return emitter.listenerCount(type);
  } else {
    return listenerCount.call(emitter, type);
  }
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
