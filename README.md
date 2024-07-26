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


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# Mode

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> [F][f-distribution] distribution [mode][mode].

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

The [mode][mode] for a [F][f-distribution] random variable with numerator degrees of freedom `d1` and denominator degrees of freedom `d2` is

<!-- <equation class="equation" label="eq:f_mode" align="center" raw="\operatorname{mode}\left( X \right) = \frac{d_{1}-2}{d_{1}} \; \frac{d_{2}}{d_{2}+2}" alt="Mode for an F distribution."> -->

```math
\mathop{\mathrm{mode}}\left( X \right) = \frac{d_{1}-2}{d_{1}} \; \frac{d_{2}}{d_{2}+2}
```

<!-- <div class="equation" align="center" data-raw-text="\operatorname{mode}\left( X \right) = \frac{d_{1}-2}{d_{1}} \; \frac{d_{2}}{d_{2}+2}" data-equation="eq:f_mode">
    <img src="https://cdn.jsdelivr.net/gh/stdlib-js/stdlib@51534079fef45e990850102147e8945fb023d1d0/lib/node_modules/@stdlib/stats/base/dists/f/mode/docs/img/equation_f_mode.svg" alt="Mode for an F distribution.">
    <br>
</div> -->

<!-- </equation> -->

for `d1 > 2` and `d2 > 0`. Otherwise, the mode is not defined.

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->



<section class="usage">

## Usage

```javascript
import mode from 'https://cdn.jsdelivr.net/gh/stdlib-js/stats-base-dists-f-mode@v0.2.2-esm/index.mjs';
```

#### mode( d1, d2 )

Returns the [mode][mode] of a [F][f-distribution] distribution with parameters `d1` (numerator degrees of freedom) and `d2` (denominator degrees of freedom).

```javascript
var v = mode( 4.0, 5.0 );
// returns ~0.357

v = mode( 4.0, 12.0 );
// returns ~0.429

v = mode( 8.0, 4.0 );
// returns 0.5
```

If provided `NaN` as any argument, the function returns `NaN`.

```javascript
var v = mode( NaN, 3.0 );
// returns NaN

v = mode( 3.0, NaN );
// returns NaN
```

If provided `d1 <= 2`, the function returns `NaN`.

```javascript
var v = mode( 1.0, 3.0 );
// returns NaN

v = mode( -1.0, 3.0 );
// returns NaN
```

If provided `d2 <= 0`, the function returns `NaN`.

```javascript
var v = mode( 3.0, 0.0 );
// returns NaN

v = mode( 3.0, -1.0 );
// returns NaN
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

import randu from 'https://cdn.jsdelivr.net/gh/stdlib-js/random-base-randu@esm/index.mjs';
import EPS from 'https://cdn.jsdelivr.net/gh/stdlib-js/constants-float64-eps@esm/index.mjs';
import mode from 'https://cdn.jsdelivr.net/gh/stdlib-js/stats-base-dists-f-mode@v0.2.2-esm/index.mjs';

var d1;
var d2;
var v;
var i;

for ( i = 0; i < 10; i++ ) {
    d1 = ( randu()*10.0 ) + EPS;
    d2 = ( randu()*10.0 ) + EPS;
    v = mode( d1, d2 );
    console.log( 'd1: %d, d2: %d, mode(X;d1,d2): %d', d1.toFixed( 4 ), d2.toFixed( 4 ), v.toFixed( 4 ) );
}

</script>
</body>
</html>
```

</section>

<!-- /.examples -->

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

Copyright &copy; 2016-2024. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/stats-base-dists-f-mode.svg
[npm-url]: https://npmjs.org/package/@stdlib/stats-base-dists-f-mode

[test-image]: https://github.com/stdlib-js/stats-base-dists-f-mode/actions/workflows/test.yml/badge.svg?branch=v0.2.2
[test-url]: https://github.com/stdlib-js/stats-base-dists-f-mode/actions/workflows/test.yml?query=branch:v0.2.2

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/stats-base-dists-f-mode/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/stats-base-dists-f-mode?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/stats-base-dists-f-mode.svg
[dependencies-url]: https://david-dm.org/stdlib-js/stats-base-dists-f-mode/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/stats-base-dists-f-mode/tree/deno
[deno-readme]: https://github.com/stdlib-js/stats-base-dists-f-mode/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/stats-base-dists-f-mode/tree/umd
[umd-readme]: https://github.com/stdlib-js/stats-base-dists-f-mode/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/stats-base-dists-f-mode/tree/esm
[esm-readme]: https://github.com/stdlib-js/stats-base-dists-f-mode/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/stats-base-dists-f-mode/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/stats-base-dists-f-mode/main/LICENSE

[f-distribution]: https://en.wikipedia.org/wiki/F_distribution

[mode]: https://en.wikipedia.org/wiki/Mode_%28statistics%29

</section>

<!-- /.links -->
