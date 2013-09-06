threex.windowresize
===================

threex.windowresize is a three.js extension to help you handle window resize.

Here is a [basic example](http://jeromeetienne.github.io/threex.windowresize/examples/basic.html) and its [source](https://github.com/jeromeetienne/threex.windowresize/blob/master/examples/basic.html).
Another [example with devicePixelRatio](http://jeromeetienne.github.io/threex.windowresize/examples/devicepixelratio.html) and its [source](https://github.com/jeromeetienne/threex.windowresize/blob/master/examples/devicepixelratio.html)

How To Install It
=================

You can install it manually. Just do 

```html
<script src='threex.windowresize.js'></script>
```

You can install with [bower](http://bower.io/).

```bash
bower install threex.windowresize
```

then you add that in your html

```html
<script src="bower_components/threex.windowresize/threex.windowresize.js"></script>
```

## How To Use

You just have to instanciate the object. Then whenever you resize the window,
it will resize the renderer canvas and adjust the camera accordingly.

```javascript
var winResize	= new THREEx.WindowResize(renderer, camera)
```

If you need to destroy it at one point, just do ```winResize.destroy();```.
It fit well with devicePixelRatio, see an example below

```javascript
renderer.devicePixelRatio	= 1/4
winResize.trigger()
```