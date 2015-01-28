# queried [![Build Status](https://travis-ci.org/dfcreative/queried.svg?branch=master)](https://travis-ci.org/dfcreative/queried) [![Code Climate](https://codeclimate.com/github/dfcreative/queried/badges/gpa.svg)](https://codeclimate.com/github/dfcreative/queried)

_Queried_ is tiny normalized query selector. It just wraps native `querySelector` and provides hooks for custom pseudos. Basically it polyfills CSS4 pseudos, but might be used to implement other pseudos, like jQuery ones or query-relative.

1. Polyfills all CSS4 pseudos: `:has`, `:scope`, `:root`.

2. Fixes immediate children selector `> *`, which is unavailable in _query_.

3. Returns `Array` instead of `NodeList` in multiple query, so you can do `forEach` on result.

7. Accepts other elements as a selector, for example, to find within a set.

7. Fully compliant with [query](https://github.com/component/query).


Use it if you need CSS4 pseudos or other specific pseudos.

Otherwise take a look at analogs:

* query-component
* dom-select
* qwery
* domy-element
* query-relative
* jquery


`$ npm install queried`

```js
var q = require('queried');

//select each div having `a` with `span` inside as immediate children.
q.all('div:has(a:has(span))');
```

# API

Fully compliant with [query-component](https://npmjs.org/package/query-component).

| Method | Description |
|---|---|
| **query(selector, el = document)** | Query a single element by selector |
| **query.all(selector, el = document)** | Query list of elements by selector |
| **query.registerFilter(name, filterFn)** | Register a new filtering pseudo |
| **query.registerMapper(name, mapperFn)** | Register a new mapping pseudo |




[![NPM](https://nodei.co/npm/queried.png?downloads=true&downloadRank=true&stars=true)](https://nodei.co/npm/queried/)

<a href="UNLICENSE"><img src="http://upload.wikimedia.org/wikipedia/commons/6/62/PD-icon.svg" width="20"/></a>