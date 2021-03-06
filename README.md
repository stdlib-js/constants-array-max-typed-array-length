<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->

# Maximum Typed Array Length

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Maximum length for a typed array.

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->

<section class="installation">

## Installation

```bash
npm install @stdlib/constants-array-max-typed-array-length
```

Alternatively,

-   To load the package in a website via a `script` tag without installation and bundlers, use the [ES Module][es-module] available on the [`esm` branch][esm-url].
-   If you are using Deno, visit the [`deno` branch][deno-url].
-   For use in Observable, or in browser/node environments, use the [Universal Module Definition (UMD)][umd] build available on the [`umd` branch][umd-url].

The [branches.md][branches-url] file summarizes the available branches and displays a diagram illustrating their relationships.

</section>

<section class="usage">

## Usage

```javascript
var MAX_TYPED_ARRAY_LENGTH = require( '@stdlib/constants-array-max-typed-array-length' );
```

#### MAX_TYPED_ARRAY_LENGTH

Maximum length for a typed array.

```javascript
var len = MAX_TYPED_ARRAY_LENGTH;
// returns 9007199254740991
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- Package usage examples. -->

<section class="examples">

## Examples

<!-- eslint-disable stdlib/new-cap-error -->

<!-- eslint no-undef: "error" -->

```javascript
var ctors = require( '@stdlib/array-ctors' );
var MAX_TYPED_ARRAY_LENGTH = require( '@stdlib/constants-array-max-typed-array-length' );

function fill( dtype, len, value ) {
    var ctor;
    var arr;
    var i;
    if ( len > MAX_TYPED_ARRAY_LENGTH ) {
        throw new RangeError( 'invalid argument. The maximum length for a typed array is '+MAX_TYPED_ARRAY_LENGTH+'.' );
    }
    ctor = ctors( dtype );
    arr = new ctor( len );
    for ( i = 0; i < len; i++ ) {
        arr[ i ] = value;
    }
    return arr;
}

var arr = fill( 'float64', 10, 3.14 );
console.log( arr );

try {
    arr = fill( 'float64', 1e300, 3.14 );
} catch ( err ) {
    console.error( err.message );
}
```

</section>

<!-- /.examples -->

<!-- Section to include cited references. If references are included, add a horizontal rule *before* the section. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="references">

</section>

<!-- /.references -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   <span class="package-name">[`@stdlib/constants/array/max-array-length`][@stdlib/constants/array/max-array-length]</span><span class="delimiter">: </span><span class="description">maximum length for a generic array.</span>

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2022. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/constants-array-max-typed-array-length.svg
[npm-url]: https://npmjs.org/package/@stdlib/constants-array-max-typed-array-length

[test-image]: https://github.com/stdlib-js/constants-array-max-typed-array-length/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/constants-array-max-typed-array-length/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/constants-array-max-typed-array-length/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/constants-array-max-typed-array-length?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/constants-array-max-typed-array-length.svg
[dependencies-url]: https://david-dm.org/stdlib-js/constants-array-max-typed-array-length/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/constants-array-max-typed-array-length/tree/deno
[umd-url]: https://github.com/stdlib-js/constants-array-max-typed-array-length/tree/umd
[esm-url]: https://github.com/stdlib-js/constants-array-max-typed-array-length/tree/esm
[branches-url]: https://github.com/stdlib-js/constants-array-max-typed-array-length/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/constants-array-max-typed-array-length/main/LICENSE

<!-- <related-links> -->

[@stdlib/constants/array/max-array-length]: https://github.com/stdlib-js/constants-array-max-array-length

<!-- </related-links> -->

</section>

<!-- /.links -->
