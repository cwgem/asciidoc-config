## Introduction ##

This is a configuration file for asciidoc XHTML output. I created it due to the fact that there were a substantial amount of <div>s in the stock XHTML module. This made the output code very difficult to read. Also divs are not needed in many cases as the content within are block level elements which can accept various style attributes all the same. Please note that this is customized for my specific use, and items such as tables have not been addressed yet. Also note the following:

* I have a Creative Commons footer badge added in
* If the `resetcss` attribute is included it includes a `reset.css` file for CSS reset (I recommend the [YUI 3 Reset CSS file](http://yuilibrary.com/yui/docs/cssreset/))
* A CSS file which targets this output is a work in progress

## Requirements ##

This configuration is run against [asciidoc 8.6.8](http://www.methods.co.nz/asciidoc/).

## Installation ##

1. Copy `xhtml-lite.conf` to the asciidoc shared directory, which in most cases will be `/usr/share/asciidoc`
2. The CSS (in progress) will need to be copied to the `/css` path on the server
3. JS files should go to the `/js` path on the server
4. Image files should go to the `/images` directory on the server

## Usage ##

This is a sample run I use to build the HTML for my website:

    asciidoc -a pygments -a badges -a icons -a iconsdir=/images -a linkcss -a stylesdir=/css -a disable-javascript -a resetcss -b xhtml-lite --theme modern -O index.html sources/index.asciidoc

Be aware that I have Javascript disabled as my needs are very minimal. 

## License ##

This project is licensed under the MIT license, a copy of which can be found in the LICENSE file.

Copyright (c) 2013 Chris White.
Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## Support ##

As this is still something meant to be custom to my use, I recommend forking this repository and making changes there. If you feel there as a generic enhancement that would be beneficial, feel free to make a [pull request](https://github.com/cwgem/asciidoc-config/pulls).

## Author ##

This project is created by Chris White (@cwgem)
