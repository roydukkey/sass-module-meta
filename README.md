# sass-meta

[![Release Version](https://img.shields.io/npm/v/sass-meta.svg)](https://www.npmjs.com/package/sass-meta)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

This Sass module provides more advanced meta functions.

## Install

### Requires

Install the package:

```bash
npm install sass-meta
```

Use the package like any other Sass module:

```scss
@use 'sass-meta';
```

Depending on your setup, you may need to configure `node_modules` as include path:

```js
const sass = require('sass');

sass.render({
  file: scss_filename,
  includePaths: ['node_modules']
});
```

## Public API

<dl>

  <dt><a href="//github.com/roydukkey/sass-module-meta/tree/master/src/meta/_call-or-reference.sass"><code>call-or-reference ( $function, $args... )</code></a></dt>
  <dd>Allows a function to return its reference when no parameters are provided, otherwise maintaining its regular behavior.</dd>

  <dt><a href="//github.com/roydukkey/sass-module-meta/tree/master/src/meta/_get-keyword.sass"><code>get-keyword ( $args, $name [, $default] )</code></a></dt>
  <dd>Gets the value of the named parameter from the given argument list, otherwise providing a default value.</dd>

</dl>

Don't see the function you're looking for? Request a [new feature](//github.com/roydukkey/sass-module-meta/issues/new) describing a use case.

## Combined API

In order to avoid constantly declaring both the native 'sass:meta' module and this library, the combined API has been added which merges the two.

```scss
// Rather than using both modules separately...
@use 'sass-meta';
@use 'sass:meta';

// ...this statement will accomplish the same thing.
@use 'sass-meta/meta';
```
