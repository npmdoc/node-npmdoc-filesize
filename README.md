# api documentation for  [filesize (v3.5.6)](http://filesizejs.com)  [![npm package](https://img.shields.io/npm/v/npmdoc-filesize.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-filesize) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-filesize.svg)](https://travis-ci.org/npmdoc/node-npmdoc-filesize)
#### JavaScript library to generate a human readable String describing the file size

[![NPM](https://nodei.co/npm/filesize.png?downloads=true)](https://www.npmjs.com/package/filesize)

[![apidoc](https://npmdoc.github.io/node-npmdoc-filesize/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-filesize_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-filesize/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-filesize/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-filesize/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Jason Mulligan",
        "email": "jason.mulligan@avoidwork.com"
    },
    "bugs": {
        "url": "https://github.com/avoidwork/filesize.js/issues"
    },
    "dependencies": {},
    "description": "JavaScript library to generate a human readable String describing the file size",
    "devDependencies": {
        "babel-preset-es2015": "~6.18.0",
        "grunt": "~1.0.1",
        "grunt-babel": "~6.0.0",
        "grunt-cli": "~1.2.0",
        "grunt-contrib-concat": "~1.0.1",
        "grunt-contrib-nodeunit": "~1.0.0",
        "grunt-contrib-uglify": "~2.0.0",
        "grunt-contrib-watch": "~1.0.0",
        "grunt-eslint": "~19.0.0"
    },
    "directories": {},
    "dist": {
        "shasum": "5fd98f3eac94ec9516ef8ed5782fad84a01a0a1a",
        "tarball": "https://registry.npmjs.org/filesize/-/filesize-3.5.6.tgz"
    },
    "engines": {
        "node": ">= 0.4.0"
    },
    "gitHead": "77db5467b33a5ae44d1dec83bcbbbd58732cd815",
    "homepage": "http://filesizejs.com",
    "keywords": [
        "file",
        "filesize",
        "size",
        "readable",
        "file system",
        "bytes",
        "diff"
    ],
    "license": "BSD-3-Clause",
    "main": "lib/filesize",
    "maintainers": [
        {
            "name": "avoidwork",
            "email": "jason@attack.io"
        }
    ],
    "name": "filesize",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/avoidwork/filesize.js.git"
    },
    "scripts": {
        "test": "grunt test"
    },
    "version": "3.5.6"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module filesize](#apidoc.module.filesize)
1.  [function <span class="apidocSignatureSpan">filesize.</span>partial (opt)](#apidoc.element.filesize.partial)



# <a name="apidoc.module.filesize"></a>[module filesize](#apidoc.module.filesize)

#### <a name="apidoc.element.filesize.partial"></a>[function <span class="apidocSignatureSpan">filesize.</span>partial (opt)](#apidoc.element.filesize.partial)
- description and source-code
```javascript
partial = function (opt) {
		return function (arg) {
			return filesize(arg, opt);
		};
	}
```
- example usage
```shell
...
filesize(1024, {output: "exponent"}); // 1
filesize(265318, {standard: "iec"});  // "259.1 KiB"
filesize(265318, {standard: "iec", fullform: true}); // "259.1 kibibytes"
filesize(12, {fullform: true, fullforms: ["байтов"]});  // "12 байтов"
'''

## Partial Application
'filesize.partial()' takes the second parameter of 'filesize()' and returns a new function with the configuration applied
upon execution. This can be used to reduce 'Object' creation if you call 'filesize()' without caching the 'descriptor'
in lexical scope.

'''javascript
const size = filesize.partial({standard: "iec"});

size(265318); // "259.1 KiB"
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
