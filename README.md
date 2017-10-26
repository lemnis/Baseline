# Base

## Installation

There are two imports to choose from. The default `scss/base` comes with
un-prefixed versions of the core API functions.
If you want Base to be name-spaced, import `scss/base-prefix` instead.

```scss
// un-prefixed functions
@import '<path-to>/base/scss/base';

// susy-prefixed functions
@import '<path-to>/base/scss/base-prefix';
```

## Starting guide using base

```scss
@import "path-to-base";

$base: (
	cap-height: .7 // cap-height of your font
)

h1 {
	$font-size: 4rem;
	font-size: $font-size;
	line-height: line-height($font-size);
	margin-top: top($font-size) + row(); // top offset + extra row of white space
	margin-bottom: bottom($font-size);
}
```

[See the full documentation](//lemnis.github.io/baseline)

## Credits

* [Susy](https://github.com/oddbird/susy/) - Lots of code is based on their internal structure and I reused lots of their comments.

## Todo

* add advise for margin collapsing
* add more tests
* create more debug-image options
* allow calculation with a different `vertical-align`