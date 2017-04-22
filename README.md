# npmdoc-url-pattern

#### api documentation for  [url-pattern (v1.0.3)](http://github.com/snd/url-pattern)  [![npm package](https://img.shields.io/npm/v/npmdoc-url-pattern.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-url-pattern) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-url-pattern.svg)](https://travis-ci.org/npmdoc/node-npmdoc-url-pattern)

#### easier than regex string matching patterns for urls and other strings. turn strings into data or data into strings.

[![NPM](https://nodei.co/npm/url-pattern.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/url-pattern)

- [https://npmdoc.github.io/node-npmdoc-url-pattern/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-url-pattern/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-url-pattern/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-url-pattern/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-url-pattern/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-url-pattern/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Maximilian Krüger",
        "url": "http://github.com/snd"
    },
    "bugs": {
        "url": "http://github.com/snd/url-pattern/issues"
    },
    "contributors": [
        {
            "name": "Andrey Popp",
            "url": "https://github.com/andreypopp"
        },
        {
            "name": "Samuel Reed",
            "url": "https://github.com/STRML"
        },
        {
            "name": "Michael Trotter",
            "url": "https://github.com/spicydonuts"
        },
        {
            "name": "Kate Hudson",
            "url": "https://github.com/k88hudson"
        },
        {
            "name": "caasi Huang",
            "url": "https://github.com/caasi"
        }
    ],
    "dependencies": {},
    "description": "easier than regex string matching patterns for urls and other strings. turn strings into data or data into strings.",
    "devDependencies": {
        "codecov.io": "0.1.6",
        "coffee-script": "1.10.0",
        "coffeeify": "2.0.1",
        "coffeetape": "1.0.1",
        "istanbul": "0.4.1",
        "tape": "4.2.2",
        "zuul": "3.8.0"
    },
    "directories": {},
    "dist": {
        "shasum": "0409292471b24f23c50d65a47931793d2b5acfc1",
        "tarball": "https://registry.npmjs.org/url-pattern/-/url-pattern-1.0.3.tgz"
    },
    "engines": {
        "node": ">=0.12.0"
    },
    "gitHead": "195d77082e438bcacaf095ecb812d80eeac456ae",
    "homepage": "http://github.com/snd/url-pattern",
    "keywords": [
        "url",
        "string",
        "matching",
        "pattern",
        "matching",
        "routing",
        "route",
        "regex",
        "match",
        "segment",
        "parsing",
        "parser",
        "parse",
        "combinator",
        "combinators",
        "custom",
        "customizable",
        "filepath",
        "path",
        "domain",
        "separator",
        "stringify",
        "generate",
        "text",
        "processing"
    ],
    "license": "MIT",
    "main": "lib/url-pattern",
    "maintainers": [
        {
            "name": "snd"
        }
    ],
    "name": "url-pattern",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/snd/url-pattern.git"
    },
    "scripts": {
        "compile": "coffee --bare --compile --output lib src",
        "prepublish": "npm run compile",
        "pretest": "npm run compile",
        "test": "coffeetape test/*",
        "test-in-browsers": "zuul test/*",
        "test-with-coverage": "istanbul cover coffeetape test/* && cat ./coverage/coverage.json | ./node_modules/codecov.io/bin/codecov.io.js",
        "test-zuul-local": "zuul --local 8080 test/*"
    },
    "typings": "index.d.ts",
    "version": "1.0.3",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
