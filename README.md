# api documentation for  [better-console (v1.0.0)](https://github.com/mohsen1/better-console#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-better-console.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-better-console) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-better-console.svg)](https://travis-ci.org/npmdoc/node-npmdoc-better-console)
#### A better console for Node.js

[![NPM](https://nodei.co/npm/better-console.png?downloads=true)](https://www.npmjs.com/package/better-console)

[![apidoc](https://npmdoc.github.io/node-npmdoc-better-console/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-better-console_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-better-console/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-better-console/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-better-console/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Mohsen Azimi"
    },
    "bugs": {
        "url": "https://github.com/mohsen1/better-console/issues"
    },
    "dependencies": {
        "chalk": "^1.1.3",
        "cli-table": "~0.3.1"
    },
    "description": "A better console for Node.js",
    "devDependencies": {},
    "directories": {},
    "dist": {
        "shasum": "cd696fa385eba396b8e0fdf54f75afddda6dd2a5",
        "tarball": "https://registry.npmjs.org/better-console/-/better-console-1.0.0.tgz"
    },
    "gitHead": "f60aef580e95e1ab5649ec320b5f445279d74829",
    "homepage": "https://github.com/mohsen1/better-console#readme",
    "keywords": [
        "console"
    ],
    "license": "BSD",
    "main": "index.js",
    "maintainers": [
        {
            "name": "mohsen",
            "email": "msnazi@gmail.com"
        }
    ],
    "name": "better-console",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/mohsen1/better-console.git"
    },
    "scripts": {
        "test": "node test.js"
    },
    "version": "1.0.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module better-console](#apidoc.module.better-console)
1.  [function <span class="apidocSignatureSpan">better-console.</span>assert (assertion)](#apidoc.element.better-console.assert)
1.  [function <span class="apidocSignatureSpan">better-console.</span>clear ()](#apidoc.element.better-console.clear)
1.  [function <span class="apidocSignatureSpan">better-console.</span>count (toCount)](#apidoc.element.better-console.count)
1.  [function <span class="apidocSignatureSpan">better-console.</span>debug ()](#apidoc.element.better-console.debug)
1.  [function <span class="apidocSignatureSpan">better-console.</span>dir ()](#apidoc.element.better-console.dir)
1.  [function <span class="apidocSignatureSpan">better-console.</span>error ()](#apidoc.element.better-console.error)
1.  [function <span class="apidocSignatureSpan">better-console.</span>info ()](#apidoc.element.better-console.info)
1.  [function <span class="apidocSignatureSpan">better-console.</span>log ()](#apidoc.element.better-console.log)
1.  [function <span class="apidocSignatureSpan">better-console.</span>table ()](#apidoc.element.better-console.table)
1.  [function <span class="apidocSignatureSpan">better-console.</span>time ()](#apidoc.element.better-console.time)
1.  [function <span class="apidocSignatureSpan">better-console.</span>timeEnd ()](#apidoc.element.better-console.timeEnd)
1.  [function <span class="apidocSignatureSpan">better-console.</span>trace ()](#apidoc.element.better-console.trace)
1.  [function <span class="apidocSignatureSpan">better-console.</span>warn ()](#apidoc.element.better-console.warn)



# <a name="apidoc.module.better-console"></a>[module better-console](#apidoc.module.better-console)

#### <a name="apidoc.element.better-console.assert"></a>[function <span class="apidocSignatureSpan">better-console.</span>assert (assertion)](#apidoc.element.better-console.assert)
- description and source-code
```javascript
assert = function (assertion){
  // todo: for now we are cheating, it's just console.erroring and then
  // leave console.asset to do it's job. actual todo: print what
  // console.assert prints just make first line red
  if (!assertion){
    logWithColor('red', ['AssertionError: false == true']);
    console.assert(assertion);
  }
}
```
- example usage
```shell
...
// it Writes red warning and throws assertion error
assert: function(assertion){
  // todo: for now we are cheating, it's just console.erroring and then
  // leave console.asset to do it's job. actual todo: print what
  // console.assert prints just make first line red
  if (!assertion){
    logWithColor('red', ['AssertionError: false == true']);
    console.assert(assertion);
  }
},

// Writes number of times each argument is called with blue color
count: function(toCount){
  var toCountString = toCount.toString && toCount.toString(),
      log;
...
```

#### <a name="apidoc.element.better-console.clear"></a>[function <span class="apidocSignatureSpan">better-console.</span>clear ()](#apidoc.element.better-console.clear)
- description and source-code
```javascript
clear = function (){
   process.stdout.write('\u001B[2J\u001B[0;0f');
}
```
- example usage
```shell
...




var console = require('./index');

console.log('Something');
console.clear();
console.info('Console should be clean now');

console.log('Log');
console.log('A string');
console.log('A manipulated string (%s) with number: %d', 'apple', 42);
console.log(1);
console.log(true);
...
```

#### <a name="apidoc.element.better-console.count"></a>[function <span class="apidocSignatureSpan">better-console.</span>count (toCount)](#apidoc.element.better-console.count)
- description and source-code
```javascript
count = function (toCount){
  var toCountString = toCount.toString && toCount.toString(),
      log;

  if (countBuffer[toCountString] == null){
    countBuffer[toCountString] = 0;
  }else{
    countBuffer[toCountString] += 1;
  }

  log = toCountString + ': ' + countBuffer[toCountString];
  logWithColor('blue', [log]);
}
```
- example usage
```shell
...
console.error(true);
console.error({ me: 1 });
console.error([1, 2, 3]);
console.error('');



console.count('me');
console.count('me');

var arr = [
  ['a', 'b', 'c', 'd'],
  ['e', 'f', 'h', 'j']
];
console.table(arr);
...
```

#### <a name="apidoc.element.better-console.debug"></a>[function <span class="apidocSignatureSpan">better-console.</span>debug ()](#apidoc.element.better-console.debug)
- description and source-code
```javascript
debug = function (){
  console.log.apply(this, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.better-console.dir"></a>[function <span class="apidocSignatureSpan">better-console.</span>dir ()](#apidoc.element.better-console.dir)
- description and source-code
```javascript
dir = function (){
  console.dir.apply(this, arguments);
}
```
- example usage
```shell
...

console.log("This is a log information");
console.warn("Warning!");
console.info("Information");
console.table([ [1,2], [3,4] ]);
console.time("Timer");
console.timeEnd("Timer");
console.dir(myObject);

'''

## Methods

### 'console.log', 'console.warn', 'console.error', 'console.info', 'console.debug', 'console.dir', 'console.trace'
These methods work exactly same as native console methods but with colors for 'warn', 'info' or 'error'
...
```

#### <a name="apidoc.element.better-console.error"></a>[function <span class="apidocSignatureSpan">better-console.</span>error ()](#apidoc.element.better-console.error)
- description and source-code
```javascript
error = function (){
  logWithColor('red', arguments, true);
}
```
- example usage
```shell
...
var util = require('util');
var logTable = require('./log_table');
var countBuffer = {};

function logWithColor(color, args, isError){
  var log = util.format.apply(this, args);
  if(isError)
    console.error(chalk[color](log));
  else
    console.log(chalk[color](log));
}


module.exports = {
...
```

#### <a name="apidoc.element.better-console.info"></a>[function <span class="apidocSignatureSpan">better-console.</span>info ()](#apidoc.element.better-console.info)
- description and source-code
```javascript
info = function (){
  logWithColor('blue', arguments);
}
```
- example usage
```shell
...
You can override 'console' object itself or assign better console to another variable. It's completely safe to override the native
 console object because better console calls native console methods for methods that are already available in it.

'''
var console = require('better-console');

console.log("This is a log information");
console.warn("Warning!");
console.info("Information");
console.table([ [1,2], [3,4] ]);
console.time("Timer");
console.timeEnd("Timer");
console.dir(myObject);

'''
...
```

#### <a name="apidoc.element.better-console.log"></a>[function <span class="apidocSignatureSpan">better-console.</span>log ()](#apidoc.element.better-console.log)
- description and source-code
```javascript
log = function (){
  console.log.apply(this, arguments);
}
```
- example usage
```shell
...
## How to use it

You can override 'console' object itself or assign better console to another variable. It's completely safe to override the native
 console object because better console calls native console methods for methods that are already available in it.

'''
var console = require('better-console');

console.log("This is a log information");
console.warn("Warning!");
console.info("Information");
console.table([ [1,2], [3,4] ]);
console.time("Timer");
console.timeEnd("Timer");
console.dir(myObject);
...
```

#### <a name="apidoc.element.better-console.table"></a>[function <span class="apidocSignatureSpan">better-console.</span>table ()](#apidoc.element.better-console.table)
- description and source-code
```javascript
table = function (){
  logTable.apply(this, arguments);
}
```
- example usage
```shell
...

'''
var console = require('better-console');

console.log("This is a log information");
console.warn("Warning!");
console.info("Information");
console.table([ [1,2], [3,4] ]);
console.time("Timer");
console.timeEnd("Timer");
console.dir(myObject);

'''

## Methods
...
```

#### <a name="apidoc.element.better-console.time"></a>[function <span class="apidocSignatureSpan">better-console.</span>time ()](#apidoc.element.better-console.time)
- description and source-code
```javascript
time = function (){
  console.time.apply(this, arguments);
}
```
- example usage
```shell
...
'''
var console = require('better-console');

console.log("This is a log information");
console.warn("Warning!");
console.info("Information");
console.table([ [1,2], [3,4] ]);
console.time("Timer");
console.timeEnd("Timer");
console.dir(myObject);

'''

## Methods
...
```

#### <a name="apidoc.element.better-console.timeEnd"></a>[function <span class="apidocSignatureSpan">better-console.</span>timeEnd ()](#apidoc.element.better-console.timeEnd)
- description and source-code
```javascript
timeEnd = function (){
  console.timeEnd.apply(this, arguments);
}
```
- example usage
```shell
...
var console = require('better-console');

console.log("This is a log information");
console.warn("Warning!");
console.info("Information");
console.table([ [1,2], [3,4] ]);
console.time("Timer");
console.timeEnd("Timer");
console.dir(myObject);

'''

## Methods

### 'console.log', 'console.warn', 'console.error', 'console.info', 'console.debug', 'console.dir', 'console.trace'
...
```

#### <a name="apidoc.element.better-console.trace"></a>[function <span class="apidocSignatureSpan">better-console.</span>trace ()](#apidoc.element.better-console.trace)
- description and source-code
```javascript
trace = function (){
  console.trace.apply(this, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.better-console.warn"></a>[function <span class="apidocSignatureSpan">better-console.</span>warn ()](#apidoc.element.better-console.warn)
- description and source-code
```javascript
warn = function (){
  logWithColor('yellow', arguments, true);
}
```
- example usage
```shell
...

You can override 'console' object itself or assign better console to another variable. It's completely safe to override the native
 console object because better console calls native console methods for methods that are already available in it.

'''
var console = require('better-console');

console.log("This is a log information");
console.warn("Warning!");
console.info("Information");
console.table([ [1,2], [3,4] ]);
console.time("Timer");
console.timeEnd("Timer");
console.dir(myObject);

'''
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
