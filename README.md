# Media queries for .LESS

---

### Who had this idea?

I just saw that [Rafal Bromirski](http://paranoida.com) created media queries for SCSS.
So i just wanted to port this for LESS, but with another usage.

### Browser support

Only modern browsers that support media queries.

## What's inside?

```
Requirements:
  LESS 1.3.3+


Values
---
@hdpi-value    (HDPI pixel ratio)
@mdpi-value    (MDPI pixel ratio)
@ldpi-value      (LDPI pixel ratio)
---

Presets
---
@hdpi      (HDPI Android devices)
@mdpi      (MDPI Android devices)
@ldpi      (LDPI Android devices)
---
@wp      (Windows Phone 7 and 8 devices with a resolution of 480x800 px)
@wp-hdpi       (New gen Windows Phone 8 HDPI devices with a min device width of 720px)
---
@ iphone (iPhone (2, 3G, 3GS) landscape & portrait)
@ iphone-landscape   (iPhone (2, 3G, 3GS) only landscape)
@ iphone-portrait    (iPhone (2, 3G, 3GS) only portrait)
---
@ iphone4      (iPhone (4, 4S) landscape & portrait)
@ iphone4-landscape  (iPhone (4, 4S) only landscape)
@ iphone4-portrait     (iPhone (4, 4S) only portrait)
---
@ iphone5      (iPhone (5) landscape & portrait)
@ iphone5-landscape  (iPhone (5) only landscape)
@ iphone5-portrait   (iPhone (5) only portrait)
---
@ ipad       (iPad (1, 2, Mini) landscape & portrait)
@ ipad-landscape (iPad   (iPad (1, 2, Mini) only landscape)
@ ipad-portrait    (iPad (1, 2, Mini) only portrait)
---
@ ipad-retina    (iPad (3, 4) landscape & portrait)
@ ipad-retina-landscape  (iPad (3, 4) only landscape)
@ ipad-retina-portrait   (iPad (3, 4) only portrait)
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


---
### License:

The MIT license

Copyright &copy; 2013 [Eduard Mayer](http://www.twitter.com)
Original work by [Rafal Bromirski](http://paranoida.com)

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.