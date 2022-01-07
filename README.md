# YFROBOT OLED MakeCode Package 
This is the MakeCode Package for YFROBOT OLED controller, based on the Adafruit Arduino library available [here](https://github.com/adafruit/Adafruit_SSD1306).


## Blocks
### Initialize YFROBOT OLED Display
Initializes the YFROBOT OLED display.

Sets up the YFROBOT OLED display and prepares it for use by the micro:bit.

```sig
YFOLED.init(64, 128);
```

This block must be placed before any of the ``show`` blocks.

### Show String Without Newline
Displays a string on the OLED module without a newline.

```sig
YFOLED.showString1("hello, micro:bit!")
```

The ``init`` block must be placed before this.

### Show String With Newline
Displays a string on the OLED module with a newline.

```sig
YFOLED.showString2("hello, micro:bit!")
```

The ``init`` block must be placed before this.


### Show Number Without newline
Displays a number on the OLED module without a newline.

```sig
YFOLED.showNumber1(123)
```

The ``init`` block must be placed before this.


### Show Number With Newline
Displays a number on the OLED module with a newline.

```sig
YFOLED.showNumber2(123)
```

The ``init`` block must be placed before this.


### Clear Display
Clears the display.

```sig
YFOLED.clear()
```

The ``init`` block must be placed before this.

### Draw Outlined Rectangle
Displays an outline of a rectangle.

```sig
YFOLED.drawRectangle(x,y,w,h)
```

The ``init`` block must be placed before this.


### Draw Outlined Circle
Displays an outline of a circle.

```sig
YFOLED.drawCircle(x,y,r)
```

The ``init`` block must be placed before this.


### Draw Line
Displays a line.

```sig
YFOLED.drawLine(x1,y1,x2,y2)
```

The ``init`` block must be placed before this.


### Progress bar
Displays a progress bar with a specified percentage of progress.

```sig
YFOLED.drawLoadingBar(percent)
```

The ``init`` block must be placed before this.


## Example: Counter
The following code is a simple counter that displays an increasing number every second.

```blocks
YFOLED.init(64, 128)
let item = 0
basic.forever(() => {
    basic.pause(1000)
    item += 1
    YFOLED.showNumber(item)
})
```


## License

MIT

Copyright (c) 2021, YFROBOT  


## Supported targets

* for PXT/microbit
  (The metadata above is needed for package search.)
