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

<section class="installation">

## Installation

```bash
npm install @stdlib/complex-conjf
```

</section>

<section class="usage">

## Usage

```javascript
var conjf = require( '@stdlib/complex-conjf' );
```

#### conjf( z )

Returns the [complex conjugate][complex-conjugate] of a single-precision complex floating-point number.

```javascript
var Complex64 = require( '@stdlib/complex-float32' );

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

```javascript
var Complex64 = require( '@stdlib/complex-float32' );
var randu = require( '@stdlib/random-base-randu' );
var round = require( '@stdlib/math-base-special-round' );
var conjf = require( '@stdlib/complex-conjf' );

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
```

</section>

<!-- /.examples -->

<!-- C interface documentation. -->

* * *

<section class="c">

## C APIs

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

</section>

<!-- /.intro -->

<!-- C usage documentation. -->

<section class="installation">

## Installation

```bash
npm install @stdlib/complex-conjf
```

</section>

<section class="usage">

### Usage

```c
#include "stdlib/complex/conjf.h"
```

#### stdlib_conjf( z )

Returns the [complex conjugate][complex-conjugate] of a single-precision complex floating-point number.

```c
#include "stdlib/complex/float32.h"
#include "stdlib/complex/realf.h"
#include "stdlib/complex/imagf.h"

stdlib_complex64_t z = stdlib_complex64( 5.0f, 2.0f );

// ...

stdlib_complex64_t v = stdlib_conjf( z );

float re = stdlib_realf( v );
// returns 5.0f

float im = stdlib_imagf( v );
// returns -2.0f
```

The function accepts the following arguments:

-   **z**: `[in] stdlib_complex64_t` single-precision complex floating-point number.

```c
stdlib_complex64_t stdlib_conjf( const stdlib_complex64_t z );
```

</section>

<!-- /.usage -->

<!-- C API usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- C API usage examples. -->

<section class="examples">

### Examples

```c
#include "stdlib/complex/conjf.h"
#include "stdlib/complex/realf.h"
#include "stdlib/complex/imagf.h"
#include "stdlib/complex/float32.h"
#include <stdio.h>

int main() {
    stdlib_complex64_t x[] = {
        stdlib_complex64( 5.0f, 2.0f ),
        stdlib_complex64( -2.0f, 1.0f ),
        stdlib_complex64( 0.0f, -0.0f ),
        stdlib_complex64( 0.0f/0.0f, 0.0f/0.0f )
    };

    stdlib_complex64_t z;
    stdlib_complex64_t v;
    int i;
    for ( i = 0; i < 4; i++ ) {
        z = x[ i ];
        v = stdlib_conjf( z );
        printf( "conj(%f + %fi) = %f + %fi\n", stdlib_realf( z ), stdlib_imagf( z ), stdlib_realf( v ), stdlib_imagf( v ) );
    }
}
```

</section>

<!-- /.examples -->

</section>

<!-- /.c -->

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

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2021. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/complex-conjf.svg
[npm-url]: https://npmjs.org/package/@stdlib/complex-conjf

[test-image]: https://github.com/stdlib-js/complex-conjf/actions/workflows/test.yml/badge.svg
[test-url]: https://github.com/stdlib-js/complex-conjf/actions/workflows/test.yml

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

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/complex-conjf/main/LICENSE

[complex-conjugate]: https://en.wikipedia.org/wiki/Complex_conjugate

</section>

<!-- /.links -->
