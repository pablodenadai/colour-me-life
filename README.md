# Colour Me Life.

> A JavaScript library for colour data visualization. 
> Easily map numbers to a smooth-transitioning colour legend.

<img src="http://i.imgur.com/UmaCjBY.jpg" width=300>

## Usage

```javascript
var ColourMeLife = require('colour-me-life');

var gradient = new ColourMeLife();
gradient
  .setSpectrum('blue', 'red')
  .setNumberRange(0, 100);
  
gradient.colourAt(13); // => hex
```

Note: This class by **default** maps the range 0 to 100 (inclusive) to the colours of the rainbow (i.e. a gradient transitioning from red to yellow to lime to blue).

## Methods

### colourAt()

```
colourMeLife.colourAt(number);
```

Returns the hex colour corresponding to the number. If number is out of range, it returns the appropriate hex colour corresponding to either the minNumber or maxNumber.

### setSpectrum()

```
colourMeLife.setSpectrum(colour1, colour2 [,colourN]);
```

Sets the new spectrum. By default, the spectrum is a rainbow. You must have a minimum of two colours, but you can specify more than two colours. Colours can be in the form 'red', 'ff0000', or '#ff0000'. For example, `rainbow.setSpectrum('red', 'yellow', 'white');` makes the "Rainbow" a colour gradient from red to yellow to white.

### setNumberRange()

```
colourMeLife.setNumberRange(minNumber, maxNumber);
```

Sets the number range of the Rainbow object. By default, it is 0 to 100.
