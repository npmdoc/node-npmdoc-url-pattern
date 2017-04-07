# api documentation for  [url-pattern (v1.0.3)](http://github.com/snd/url-pattern)  [![npm package](https://img.shields.io/npm/v/npmdoc-url-pattern.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-url-pattern) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-url-pattern.svg)](https://travis-ci.org/npmdoc/node-npmdoc-url-pattern)
#### easier than regex string matching patterns for urls and other strings. turn strings into data or data into strings.

[![NPM](https://nodei.co/npm/url-pattern.png?downloads=true)](https://www.npmjs.com/package/url-pattern)

[![apidoc](https://npmdoc.github.io/node-npmdoc-url-pattern/build/screenCapture.buildNpmdoc.browser.%2Fhome%2Ftravis%2Fbuild%2Fnpmdoc%2Fnode-npmdoc-url-pattern%2Ftmp%2Fbuild%2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-url-pattern/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-url-pattern/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-url-pattern/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Maximilian Krüger",
        "email": "kruemaxi@gmail.com",
        "url": "http://github.com/snd"
    },
    "bugs": {
        "url": "http://github.com/snd/url-pattern/issues",
        "email": "kruemaxi@gmail.com"
    },
    "contributors": [
        {
            "name": "Andrey Popp",
            "email": "8mayday@gmail.com",
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
            "name": "snd",
            "email": "kruemaxi@googlemail.com"
        }
    ],
    "name": "url-pattern",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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
    "version": "1.0.3"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module url-pattern](#apidoc.module.url-pattern)
1.  [function <span class="apidocSignatureSpan">url-pattern.</span>astNodeContainsSegmentsForProvidedParams (astNode, params, nextIndexes)](#apidoc.element.url-pattern.astNodeContainsSegmentsForProvidedParams)
1.  [function <span class="apidocSignatureSpan">url-pattern.</span>astNodeToNames (astNode)](#apidoc.element.url-pattern.astNodeToNames)
1.  [function <span class="apidocSignatureSpan">url-pattern.</span>astNodeToRegexString (astNode, segmentValueCharset)](#apidoc.element.url-pattern.astNodeToRegexString)
1.  [function <span class="apidocSignatureSpan">url-pattern.</span>concatMap (array, f)](#apidoc.element.url-pattern.concatMap)
1.  [function <span class="apidocSignatureSpan">url-pattern.</span>escapeForRegex (string)](#apidoc.element.url-pattern.escapeForRegex)
1.  [function <span class="apidocSignatureSpan">url-pattern.</span>getParam (params, key, nextIndexes, sideEffects)](#apidoc.element.url-pattern.getParam)
1.  [function <span class="apidocSignatureSpan">url-pattern.</span>keysAndValuesToObject (keys, values)](#apidoc.element.url-pattern.keysAndValuesToObject)
1.  [function <span class="apidocSignatureSpan">url-pattern.</span>newParser (options)](#apidoc.element.url-pattern.newParser)
1.  [function <span class="apidocSignatureSpan">url-pattern.</span>regexGroupCount (regex)](#apidoc.element.url-pattern.regexGroupCount)
1.  [function <span class="apidocSignatureSpan">url-pattern.</span>stringConcatMap (array, f)](#apidoc.element.url-pattern.stringConcatMap)
1.  [function <span class="apidocSignatureSpan">url-pattern.</span>stringify (astNode, params, nextIndexes)](#apidoc.element.url-pattern.stringify)
1.  object <span class="apidocSignatureSpan">url-pattern.</span>P
1.  object <span class="apidocSignatureSpan">url-pattern.</span>defaultOptions

#### [module url-pattern.P](#apidoc.module.url-pattern.P)
1.  [function <span class="apidocSignatureSpan">url-pattern.P.</span>Result (value, rest)](#apidoc.element.url-pattern.P.Result)
1.  [function <span class="apidocSignatureSpan">url-pattern.P.</span>Tagged (tag, value)](#apidoc.element.url-pattern.P.Tagged)
1.  [function <span class="apidocSignatureSpan">url-pattern.P.</span>baseMany (parser, end, stringResult, atLeastOneResultRequired, input)](#apidoc.element.url-pattern.P.baseMany)
1.  [function <span class="apidocSignatureSpan">url-pattern.P.</span>concatMany1Till (parser, end)](#apidoc.element.url-pattern.P.concatMany1Till)
1.  [function <span class="apidocSignatureSpan">url-pattern.P.</span>firstChoice ()](#apidoc.element.url-pattern.P.firstChoice)
1.  [function <span class="apidocSignatureSpan">url-pattern.P.</span>lazy (fn)](#apidoc.element.url-pattern.P.lazy)
1.  [function <span class="apidocSignatureSpan">url-pattern.P.</span>many1 (parser)](#apidoc.element.url-pattern.P.many1)
1.  [function <span class="apidocSignatureSpan">url-pattern.P.</span>pick ()](#apidoc.element.url-pattern.P.pick)
1.  [function <span class="apidocSignatureSpan">url-pattern.P.</span>regex (regex)](#apidoc.element.url-pattern.P.regex)
1.  [function <span class="apidocSignatureSpan">url-pattern.P.</span>sequence ()](#apidoc.element.url-pattern.P.sequence)
1.  [function <span class="apidocSignatureSpan">url-pattern.P.</span>string (string)](#apidoc.element.url-pattern.P.string)
1.  [function <span class="apidocSignatureSpan">url-pattern.P.</span>tag (tag, parser)](#apidoc.element.url-pattern.P.tag)



# <a name="apidoc.module.url-pattern"></a>[module url-pattern](#apidoc.module.url-pattern)

#### <a name="apidoc.element.url-pattern.astNodeContainsSegmentsForProvidedParams"></a>[function <span class="apidocSignatureSpan">url-pattern.</span>astNodeContainsSegmentsForProvidedParams (astNode, params, nextIndexes)](#apidoc.element.url-pattern.astNodeContainsSegmentsForProvidedParams)
- description and source-code
```javascript
astNodeContainsSegmentsForProvidedParams = function (astNode, params, nextIndexes) {
  var i, length;
  if (Array.isArray(astNode)) {
    i = -1;
    length = astNode.length;
    while (++i < length) {
      if (astNodeContainsSegmentsForProvidedParams(astNode[i], params, nextIndexes)) {
        return true;
      }
    }
    return false;
  }
  switch (astNode.tag) {
    case 'wildcard':
      return getParam(params, '_', nextIndexes, false) != null;
    case 'named':
      return getParam(params, astNode.value, nextIndexes, false) != null;
    case 'static':
      return false;
    case 'optional':
      return astNodeContainsSegmentsForProvidedParams(astNode.value, params, nextIndexes);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.url-pattern.astNodeToNames"></a>[function <span class="apidocSignatureSpan">url-pattern.</span>astNodeToNames (astNode)](#apidoc.element.url-pattern.astNodeToNames)
- description and source-code
```javascript
astNodeToNames = function (astNode) {
  if (Array.isArray(astNode)) {
    return concatMap(astNode, astNodeToNames);
  }
  switch (astNode.tag) {
    case 'wildcard':
      return ['_'];
    case 'named':
      return [astNode.value];
    case 'static':
      return [];
    case 'optional':
      return astNodeToNames(astNode.value);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.url-pattern.astNodeToRegexString"></a>[function <span class="apidocSignatureSpan">url-pattern.</span>astNodeToRegexString (astNode, segmentValueCharset)](#apidoc.element.url-pattern.astNodeToRegexString)
- description and source-code
```javascript
astNodeToRegexString = function (astNode, segmentValueCharset) {
  if (segmentValueCharset == null) {
    segmentValueCharset = defaultOptions.segmentValueCharset;
  }
  return '^' + baseAstNodeToRegexString(astNode, segmentValueCharset) + '$';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.url-pattern.concatMap"></a>[function <span class="apidocSignatureSpan">url-pattern.</span>concatMap (array, f)](#apidoc.element.url-pattern.concatMap)
- description and source-code
```javascript
concatMap = function (array, f) {
  var i, length, results;
  results = [];
  i = -1;
  length = array.length;
  while (++i < length) {
    results = results.concat(f(array[i]));
  }
  return results;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.url-pattern.escapeForRegex"></a>[function <span class="apidocSignatureSpan">url-pattern.</span>escapeForRegex (string)](#apidoc.element.url-pattern.escapeForRegex)
- description and source-code
```javascript
escapeForRegex = function (string) {
  return string.replace(/[-\/\\^$*+?.()|[\]{}]/g, '\\$&');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.url-pattern.getParam"></a>[function <span class="apidocSignatureSpan">url-pattern.</span>getParam (params, key, nextIndexes, sideEffects)](#apidoc.element.url-pattern.getParam)
- description and source-code
```javascript
getParam = function (params, key, nextIndexes, sideEffects) {
  var index, maxIndex, result, value;
  if (sideEffects == null) {
    sideEffects = false;
  }
  value = params[key];
  if (value == null) {
    if (sideEffects) {
      throw new Error("no values provided for key '" + key + "'");
    } else {
      return;
    }
  }
  index = nextIndexes[key] || 0;
  maxIndex = Array.isArray(value) ? value.length - 1 : 0;
  if (index > maxIndex) {
    if (sideEffects) {
      throw new Error("too few values provided for key '" + key + "'");
    } else {
      return;
    }
  }
  result = Array.isArray(value) ? value[index] : value;
  if (sideEffects) {
    nextIndexes[key] = index + 1;
  }
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.url-pattern.keysAndValuesToObject"></a>[function <span class="apidocSignatureSpan">url-pattern.</span>keysAndValuesToObject (keys, values)](#apidoc.element.url-pattern.keysAndValuesToObject)
- description and source-code
```javascript
keysAndValuesToObject = function (keys, values) {
  var i, key, length, object, value;
  object = {};
  i = -1;
  length = keys.length;
  while (++i < length) {
    key = keys[i];
    value = values[i];
    if (value == null) {
      continue;
    }
    if (object[key] != null) {
      if (!Array.isArray(object[key])) {
        object[key] = [object[key]];
      }
      object[key].push(value);
    } else {
      object[key] = value;
    }
  }
  return object;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.url-pattern.newParser"></a>[function <span class="apidocSignatureSpan">url-pattern.</span>newParser (options)](#apidoc.element.url-pattern.newParser)
- description and source-code
```javascript
newParser = function (options) {
  var U;
  U = {};
  U.wildcard = P.tag('wildcard', P.string(options.wildcardChar));
  U.optional = P.tag('optional', P.pick(1, P.string(options.optionalSegmentStartChar), P.lazy(function() {
    return U.pattern;
  }), P.string(options.optionalSegmentEndChar)));
  U.name = P.regex(new RegExp("^[" + options.segmentNameCharset + "]+"));
  U.named = P.tag('named', P.pick(1, P.string(options.segmentNameStartChar), P.lazy(function() {
    return U.name;
  })));
  U.escapedChar = P.pick(1, P.string(options.escapeChar), P.regex(/^./));
  U["static"] = P.tag('static', P.concatMany1Till(P.firstChoice(P.lazy(function() {
    return U.escapedChar;
  }), P.regex(/^./)), P.firstChoice(P.string(options.segmentNameStartChar), P.string(options.optionalSegmentStartChar), P.string
(options.optionalSegmentEndChar), U.wildcard)));
  U.token = P.lazy(function() {
    return P.firstChoice(U.wildcard, U.optional, U.named, U["static"]);
  });
  U.pattern = P.many1(P.lazy(function() {
    return U.token;
  }));
  return U;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.url-pattern.regexGroupCount"></a>[function <span class="apidocSignatureSpan">url-pattern.</span>regexGroupCount (regex)](#apidoc.element.url-pattern.regexGroupCount)
- description and source-code
```javascript
regexGroupCount = function (regex) {
  return (new RegExp(regex.toString() + '|')).exec('').length - 1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.url-pattern.stringConcatMap"></a>[function <span class="apidocSignatureSpan">url-pattern.</span>stringConcatMap (array, f)](#apidoc.element.url-pattern.stringConcatMap)
- description and source-code
```javascript
stringConcatMap = function (array, f) {
  var i, length, result;
  result = '';
  i = -1;
  length = array.length;
  while (++i < length) {
    result += f(array[i]);
  }
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.url-pattern.stringify"></a>[function <span class="apidocSignatureSpan">url-pattern.</span>stringify (astNode, params, nextIndexes)](#apidoc.element.url-pattern.stringify)
- description and source-code
```javascript
stringify = function (astNode, params, nextIndexes) {
  if (Array.isArray(astNode)) {
    return stringConcatMap(astNode, function(node) {
      return stringify(node, params, nextIndexes);
    });
  }
  switch (astNode.tag) {
    case 'wildcard':
      return getParam(params, '_', nextIndexes, true);
    case 'named':
      return getParam(params, astNode.value, nextIndexes, true);
    case 'static':
      return astNode.value;
    case 'optional':
      if (astNodeContainsSegmentsForProvidedParams(astNode.value, params, nextIndexes)) {
        return stringify(astNode.value, params, nextIndexes);
      } else {
        return '';
      }
  }
}
```
- example usage
```shell
...
pattern.match('/api/users/10'); // {id: '10'}
pattern.match('/api/users'); // {}
pattern.match('/api/products/5'); // null
'''

[generate string from pattern and values:](#stringify-patterns)
''' javascript
pattern.stringify() // '/api/users'
pattern.stringify({id: 20}) // '/api/users/20'
'''

- continuously tested in Node.js (0.12, 4.2.3 and 5.3) and all relevant browsers:
  [![Sauce Test Status](https://saucelabs.com/browser-matrix/urlpattern.svg)](https://saucelabs.com/u/urlpattern)
- [tiny single file with just under 500 lines of simple, readable, maintainable code](src/url-pattern.coffee)
- [huge test suite](test)
...
```



# <a name="apidoc.module.url-pattern.P"></a>[module url-pattern.P](#apidoc.module.url-pattern.P)

#### <a name="apidoc.element.url-pattern.P.Result"></a>[function <span class="apidocSignatureSpan">url-pattern.P.</span>Result (value, rest)](#apidoc.element.url-pattern.P.Result)
- description and source-code
```javascript
Result = function (value, rest) {
  this.value = value;
  this.rest = rest;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.url-pattern.P.Tagged"></a>[function <span class="apidocSignatureSpan">url-pattern.P.</span>Tagged (tag, value)](#apidoc.element.url-pattern.P.Tagged)
- description and source-code
```javascript
Tagged = function (tag, value) {
  this.tag = tag;
  this.value = value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.url-pattern.P.baseMany"></a>[function <span class="apidocSignatureSpan">url-pattern.P.</span>baseMany (parser, end, stringResult, atLeastOneResultRequired, input)](#apidoc.element.url-pattern.P.baseMany)
- description and source-code
```javascript
baseMany = function (parser, end, stringResult, atLeastOneResultRequired, input) {
  var endResult, parserResult, rest, results;
  rest = input;
  results = stringResult ? '' : [];
  while (true) {
    if (end != null) {
      endResult = end(rest);
      if (endResult != null) {
        break;
      }
    }
    parserResult = parser(rest);
    if (parserResult == null) {
      break;
    }
    if (stringResult) {
      results += parserResult.value;
    } else {
      results.push(parserResult.value);
    }
    rest = parserResult.rest;
  }
  if (atLeastOneResultRequired && results.length === 0) {
    return;
  }
  return new P.Result(results, rest);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.url-pattern.P.concatMany1Till"></a>[function <span class="apidocSignatureSpan">url-pattern.P.</span>concatMany1Till (parser, end)](#apidoc.element.url-pattern.P.concatMany1Till)
- description and source-code
```javascript
concatMany1Till = function (parser, end) {
  return function(input) {
    return P.baseMany(parser, end, true, true, input);
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.url-pattern.P.firstChoice"></a>[function <span class="apidocSignatureSpan">url-pattern.P.</span>firstChoice ()](#apidoc.element.url-pattern.P.firstChoice)
- description and source-code
```javascript
firstChoice = function () {
  var parsers;
  parsers = 1 <= arguments.length ? slice.call(arguments, 0) : [];
  return function(input) {
    var i, length, parser, result;
    i = -1;
    length = parsers.length;
    while (++i < length) {
      parser = parsers[i];
      result = parser(input);
      if (result != null) {
        return result;
      }
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.url-pattern.P.lazy"></a>[function <span class="apidocSignatureSpan">url-pattern.P.</span>lazy (fn)](#apidoc.element.url-pattern.P.lazy)
- description and source-code
```javascript
lazy = function (fn) {
  var cached;
  cached = null;
  return function(input) {
    if (cached == null) {
      cached = fn();
    }
    return cached(input);
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.url-pattern.P.many1"></a>[function <span class="apidocSignatureSpan">url-pattern.P.</span>many1 (parser)](#apidoc.element.url-pattern.P.many1)
- description and source-code
```javascript
many1 = function (parser) {
  return function(input) {
    return P.baseMany(parser, null, false, true, input);
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.url-pattern.P.pick"></a>[function <span class="apidocSignatureSpan">url-pattern.P.</span>pick ()](#apidoc.element.url-pattern.P.pick)
- description and source-code
```javascript
pick = function () {
  var indexes, parsers;
  indexes = arguments[0], parsers = 2 <= arguments.length ? slice.call(arguments, 1) : [];
  return function(input) {
    var array, result;
    result = P.sequence.apply(P, parsers)(input);
    if (result == null) {
      return;
    }
    array = result.value;
    result.value = array[indexes];
    return result;
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.url-pattern.P.regex"></a>[function <span class="apidocSignatureSpan">url-pattern.P.</span>regex (regex)](#apidoc.element.url-pattern.P.regex)
- description and source-code
```javascript
regex = function (regex) {
  return function(input) {
    var matches, result;
    matches = regex.exec(input);
    if (matches == null) {
      return;
    }
    result = matches[0];
    return new P.Result(result, input.slice(result.length));
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.url-pattern.P.sequence"></a>[function <span class="apidocSignatureSpan">url-pattern.P.</span>sequence ()](#apidoc.element.url-pattern.P.sequence)
- description and source-code
```javascript
sequence = function () {
  var parsers;
  parsers = 1 <= arguments.length ? slice.call(arguments, 0) : [];
  return function(input) {
    var i, length, parser, rest, result, values;
    i = -1;
    length = parsers.length;
    values = [];
    rest = input;
    while (++i < length) {
      parser = parsers[i];
      result = parser(rest);
      if (result == null) {
        return;
      }
      values.push(result.value);
      rest = result.rest;
    }
    return new P.Result(values, rest);
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.url-pattern.P.string"></a>[function <span class="apidocSignatureSpan">url-pattern.P.</span>string (string)](#apidoc.element.url-pattern.P.string)
- description and source-code
```javascript
string = function (string) {
  var length;
  length = string.length;
  return function(input) {
    if (input.slice(0, length) === string) {
      return new P.Result(string, input.slice(length));
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.url-pattern.P.tag"></a>[function <span class="apidocSignatureSpan">url-pattern.P.</span>tag (tag, parser)](#apidoc.element.url-pattern.P.tag)
- description and source-code
```javascript
tag = function (tag, parser) {
  return function(input) {
    var result, tagged;
    result = parser(input);
    if (result == null) {
      return;
    }
    tagged = new P.Tagged(tag, result.value);
    return new P.Result(tagged, result.rest);
  };
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
