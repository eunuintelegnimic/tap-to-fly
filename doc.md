# Parallax

Parallax is a plugin for easily displaying landscape background layers giving
an impression of distance by parallax scrolling.

## Initialization

You start by creating a parallax object, calling function ```createParallax```:
```
init = function()
  parallax = createParallax()
  // ...
end
```

## Adding layers

You can add layers by calling ```add``` on your parallax object:

```
  parallax.add("decor1",200,0,4)
  parallax.add("decor2",200,-40,3)
  parallax.add("decor3",200,-80,2)
```

Arguments are:

* the name of the sprite for this background layer
* the display size of the background layer ; 200 fills the screen in height
* the vertical position of your layer (y axis)
* the distance of your layer from the camera

The layers must be added in the order they will be drawn on screen, thus the more distant
layer first.

## Updating coordinates

You can update the position of the camera by setting ```x``` and ```y``` coordinates on your
parallax object, as in this example:

```
  parallax.x = 50
  parallax.y = -20
```

## Drawing

In your main draw function, simply call ```parallax.draw()``` to have the parallax layers
painted on screen.

```
draw = function()
  screen.clear()
  parallax.draw()
  
  // ... start drawing foreground content here
end
```



