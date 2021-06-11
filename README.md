### FreeCodeCamp Polygon Area Calculator Project

`shape_calculator.py` contains class `Rectangle` and an extension of the class `Square(Rectangle)`.

#### Rectangle Class

`Rectangle` objects are initialized with `width` and `height` attributes and contain the following methods:

* `set_width()` - accepts a new width as an argument
* `set_height()` - accepts a new `height` as an argument
* `get_area()`
* `get_perimeter()`
* `get_diagonal()` - calculates diagonal distance (`(width ** 2 + height ** 2) ** .5`)
* `get_picture()` - Returns a string that represents the shape using lines of "\*". The number of lines should be equal to the height and the number of "\*" in each line should be equal to the width.
* `get_amount_inside()` - Takes another shape (square or rectangle) as an argument. Returns the number of times the passed in shape could fit inside the shape (with no rotations).

#### Square Class

`Square(Rectangle)` is initialized by passing in a single side length.

##### Example:

```py
rect = shape_calculator.Rectangle(10, 5)
print(rect.get_area())
rect.set_height(3)
print(rect.get_perimeter())
print(rect)
print(rect.get_picture())

sq = shape_calculator.Square(9)
print(sq.get_area())
sq.set_side(4)
print(sq.get_diagonal())
print(sq)
print(sq.get_picture())

rect.set_height(8)
rect.set_width(16)
print(rect.get_amount_inside(sq))
```

Should return:

```
50
26
Rectangle(width=10, height=3)
**********
**********
**********

81
5.656854249492381
Square(side=4)
****
****
****
****

8
```
