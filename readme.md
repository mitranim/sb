## Overview

Short for **S**tyle-**B**ase. This is a different type of style library:

* No fancy visuals, just a blank canvas and convenient building blocks.
* Must be copied and pasted; will never break your app with a "minor" update.
* Everything is opt-in.
* Very small, very simple.

It consists of:

  * A style reset.
  * Common-sense classes for primitive properties.
  * Flexbox layout shortcuts.

It _does not include_:

  * Visual styles.
  * Complex elements.

Read `_sb.scss`, it's self-explanatory.

## Why

I've used various GUI and style frameworks, wrote a few: [1](https://mitranim.com/stylific/), [2](https://mitranim.com/stylific-lite/); collaborated on a few: [3](https://github.com/aristovn/stylebox), [4](https://github.com/purelabio/purelab-ui). None of them fully survive a switch to a new project with a new design. A fully reusable CSS core cannot be a visual framework.

This is the common denominator, the sediment, that has successfully survived being copied-and-pasted between many of my and [Purelab](http://purelab.io) projects with vastly different visual styles.

The idea of reusable elements is nice, but it doesn't work well for CSS. The idea of just grabbing a style library from NPM is nice, but it doesn't work well for CSS. Applications need to write their CSS _almost_ from scratch, and for me, this "library" is close to that threshold.

## Usage

This must be **copied and pasted** into your application. CSS libraries, even semantically versioned, are way too brittle. There's no such thing as a non-breaking change in CSS, and the application needs _full control_ over the code.

Requires SCSS. Names are unprefixed; import via `@use` for namespacing.

```scss
@use './sb/reset';
@use './sb/sb';

@include sb.all;
```

## License

https://unlicense.org

## Misc

If you have questions or suggestions, open an issue or chat me up. Contacts: https://mitranim.com/#contacts
