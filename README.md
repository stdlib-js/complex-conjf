<!--

@license Apache-2.0

Copyright (c) 2021 The Stdlib Authors.

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

# conjf

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Return the [complex conjugate][complex-conjugate] of a single-precision complex floating-point number.

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->



<section class="usage">

## Usage

```javascript
import conjf from 'https://cdn.jsdelivr.net/gh/stdlib-js/complex-conjf@esm/index.mjs';
```

#### conjf( z )

Returns the [complex conjugate][complex-conjugate] of a single-precision complex floating-point number.

```javascript
import Complex64 from 'https://cdn.jsdelivr.net/gh/stdlib-js/complex-float32@esm/index.mjs';

var z = new Complex64( 5.0, 3.0 );
var str = z.toString();
// returns '5 + 3i'

var v = conjf( z );
str = v.toString();
// returns '5 - 3i'
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

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="module">

import Complex64 from 'https://cdn.jsdelivr.net/gh/stdlib-js/complex-float32@esm/index.mjs';
import randu from 'https://cdn.jsdelivr.net/gh/stdlib-js/random-base-randu@esm/index.mjs';
import round from 'https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-round@esm/index.mjs';
import conjf from 'https://cdn.jsdelivr.net/gh/stdlib-js/complex-conjf@esm/index.mjs';

var re;
var im;
var z;
var i;

for ( i = 0; i < 100; i++ ) {
    re = round( (randu()*100.0) - 50.0 );
    im = round( (randu()*50.0) - 25.0 );
    z = new Complex64( re, im );
    console.log( 'conjf(%s) = %s', z.toString(), conjf( z ).toString() );
}

</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- C interface documentation. -->



<!-- Section to include cited references. If references are included, add a horizontal rule *before* the section. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="references">

</section>

<!-- /.references -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2023. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/complex-conjf.svg
[npm-url]: https://npmjs.org/package/@stdlib/complex-conjf

[test-image]: https://github.com/stdlib-js/complex-conjf/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/complex-conjf/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/complex-conjf/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/complex-conjf?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/complex-conjf.svg
[dependencies-url]: https://david-dm.org/stdlib-js/complex-conjf/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/complex-conjf/tree/deno
[umd-url]: https://github.com/stdlib-js/complex-conjf/tree/umd
[esm-url]: https://github.com/stdlib-js/complex-conjf/tree/esm
[branches-url]: https://github.com/stdlib-js/complex-conjf/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/complex-conjf/main/LICENSE

[complex-conjugate]: https://en.wikipedia.org/wiki/Complex_conjugate

</section>

<!-- /.links -->
