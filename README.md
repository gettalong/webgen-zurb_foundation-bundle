# ZURB Foundation framework for webgen

This is a [webgen] extension bundle that provides the [Scss standalone
version][1] of the [ZURB Foundation][2] CSS framework. This bundle
allows the easy inclusion of parts or all of the Foundation framework in
webgen websites.

[webgen]: http://webgen.gettalong.org
[1]: https://github.com/zurb/foundation/tree/scss-standalone
[2]: http://foundation.zurb.com/


# Usage

This extension bundle includes all of the Scss and Javascript files of
the Scss standalone version of ZURB Foundation.

It is recommended that you familiarize yourself with [how Foundation
works][doc].


## Scss files

The needed Scss stylesheets are provided under the `/foundation/` path:

* The `foundation.scss` file can be imported to include all the
  functionality of the Foundation framework.

* There is a sub-directory called `components/` where the individual
  component files live.

* The `normalize.scss` file that is included in ZURB Foundation
  distribution (see <http://git.io/normalize>).

*Note* that the Scss files are only available to the Sass/Scss content
processors, i.e. no nodes are created for them!

The following statements placed in any Scss stylesheet you use in your
webgen website would import the whole Foundation CSS framework:

    @import "/foundation/normalize"
    @import "/foundation/foundation"


[doc]: http://foundation.zurb.com/docs/index.html


## Javascript files

The Foundation javascript files are provided as passive nodes under the
`/javascripts/foundation/` path (e.g.
`/javascripts/foundation/foundation.dropdown.js`).

The vendored files included in the ZURB Foundation distribution are
available under the `/javascripts/foundation/vendor/` directory.


# Installation

The easiest way to install this extension bundle is by installing the
corresponding Rubygem:

    gem install webgen-zurb_foundation-bundle

If you don't use Rubygems, copy the folder
`lib/webgen/bundle/zurb_foundation` into your `ext` directory.

After that you just need to tell webgen to use this extension bundle by
adding the following line to your `ext/init.rb` file:

    load("zurb_foundation")


# Copyright and license

Copyright (c) 2013 Thomas Leitner under the MIT license (see LICENSE)

* * *

All files included from the [Scss standalone version] of ZURB Foundation
(including the vendored files) are licensed under the MIT license.
