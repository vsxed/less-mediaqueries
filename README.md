# Media queries for .LESS

---

### Who had this idea?

I just saw that [Rafal Bromirski](http://paranoida.com) created media queries for SCSS.

So i just wanted to port this for LESS, but with another usage.

### What is it?

This is just a small collection of different presets for the recognization of mobile devices in .css files.

You can import them into existing projects without the need to modify anything.

This will save your time, trust me.

### Browser support

Only modern browsers that support media queries.

## What's inside?

```
Requirements:
  LESS 1.3.3+


Values
---
@hdpi-value                  (HDPI pixel ratio)
@mdpi-value                  (MDPI pixel ratio)
@ldpi-value                  (LDPI pixel ratio)
---

Presets
---
@hdpi                        (HDPI Android devices)
@mdpi                        (MDPI Android devices)
@ldpi                        (LDPI Android devices)
---
@wp                          (Windows Phone 7 and 8 devices with a resolution of 480x800 px)
@wp-hdpi                     (New gen Windows Phone 8 HDPI devices with a min device width of 720px)
---
@ iphone                     (iPhone (2, 3G, 3GS) landscape & portrait)
@ iphone-landscape           (iPhone (2, 3G, 3GS) only landscape)
@ iphone-portrait            (iPhone (2, 3G, 3GS) only portrait)
---
@ iphone4                    (iPhone (4, 4S) landscape & portrait)
@ iphone4-landscape          (iPhone (4, 4S) only landscape)
@ iphone4-portrait           (iPhone (4, 4S) only portrait)
---
@ iphone5                    (iPhone (5) landscape & portrait)
@ iphone5-landscape          (iPhone (5) only landscape)
@ iphone5-portrait           (iPhone (5) only portrait)
---
@ ipad                       (iPad (1, 2, Mini) landscape & portrait)
@ ipad-landscape             (iPad (1, 2, Mini) only landscape)
@ ipad-portrait              (iPad (1, 2, Mini) only portrait)
---
@ ipad-retina                (iPad (3, 4) landscape & portrait)
@ ipad-retina-landscape      (iPad (3, 4) only landscape)
@ ipad-retina-portrait       (iPad (3, 4) only portrait)
---
```
## How does it work?

Those "Presets" are just pre-written @variables.

Use them in combination with the ```@media``` function provided by LESS.

## How to use?

### 1. Step:
Import ```less-mediaqueries.less```:

```
@import "../less-mediaqueries.less";
```

### 2. Step:
Use the presets just like in the following example:

```
.test-class {
  color: red;

  @media @iphone {
    color: green;
  }

  @media @hdpi {
    color: blue;
  }
}
```

This will be output:

```
.test-class {
  color: red;
}

@media only screen and (min-device-width: 320px) and (max-device-width: 480px) and (-webkit-device-pixel-ratio: 1) {
  .test-class {
    color: green;
  }
}

@media only screen and (min-device-width: 320px) and (max-device-width: 568px) and (-webkit-device-pixel-ratio: 2) and (device-aspect-ratio: 40/71) {
  .test-class {
    color: blue;
  }
}
```

You can also combine the presets to get a wider range of devices:

Input:

```
.multiple-presets {
  @media @hdpi,@mdpi {
    color: hotpink;
  }
}
```

Output:

```
@media only screen and (-webkit-min-device-pixel-ratio:  1.3 ) and (-moz-min-device-pixel-ratio:  1.3 ) and (-o-min-device-pixel-ratio:  1.3 ) and (min-resolution:  125 dpi) and (min-resolution:  1.3 dppx), only screen and (-webkit-min-device-pixel-ratio:  1 ) and (-moz-min-device-pixel-ratio:  1 ) and (-o-min-device-pixel-ratio:  1 ) and (min-resolution:  96 dpi) and (min-resolution:  1 dppx), only screen and (device-width: 320px) and (device-height: 480px) {
  .multiple-presets {
    color: hotpink;
  }
}
```

### That's it!

---
### License:

The MIT license

Copyright &copy; 2013 [Eduard Mayer](http://www.twitter.com)

Original work by [Rafal Bromirski](http://paranoida.com)

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
