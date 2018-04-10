## Overview

This is a different type of style library:

* no "styles", just a blank canvas and flexbox layout tools
* no "elements", just primitive common-sense classes
* must be copied and pasted; it will never break your application with a "minor" update

It consists of:

  * a style reset
  * common-sense classes for primitive properties
  * flexbox layout shortcuts

It _does not include_:

  * visual styles
  * complex elements

I've used various GUI and style frameworks, wrote a few: [1](https://mitranim.com/stylific/), [2](https://mitranim.com/stylific-lite/); collaborated on a few: [3](https://github.com/aristovn/stylebox), [4](https://github.com/purelabio/purelab-ui). None of them fully survive a switch to a new project with a new design. A fully reusable CSS core cannot be a visual framework.

Size: see the section below.

## Why

This is the common denominator, the sediment, that has successfully survived being copied-and-pasted between many of my and [Purelab](http://purelab.io) projects with vastly different visual styles.

The idea of reusable elements is nice, but it doesn't work well for CSS. The idea of just grabbing a style library from NPM is nice, but it doesn't work well for CSS. Applications need to write their CSS _almost_ from scratch, and for me, this "library" is close to that threshold.

## Usage

This must be **copied and pasted** into your application. I've come to believe that CSS libraries, even semantically versioned, are way too brittle. There's no such thing as a non-breaking change in CSS, and the application needs _full control_ over the code.

Requires SCSS, but is trivial to convert to CSS if needed. _Must_ be run through [Autoprefixer](https://github.com/postcss/autoprefixer).

## Size

After applying `autoprefixer` for IE >= 10 and `clean-css`, the minified size becomes around 26 KB. More than half of that are flexbox and ordering classes, which require multiple vendor-specific variations. Comment out the ones you don't use.

## Misc

If you have questions or suggestions, open an issue or chat me up. Contacts: https://mitranim.com/#contacts
