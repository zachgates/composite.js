# Composite — Module used to draw lines on canvas from points
* used to trace lines
* strictly javascript approach

##Setting Up The Canvas
```html
<canvas id="mycavas"        // set a unique id
		width="100"         // set the width  (x-axis)
		height="100"        // set the height (y-axis)
		
		// set any other attributes below
		style="border: solid 1px black;"> 
</canvas>
```

##Basic Usage — Single line
```javascript
var context = document.getElementById('mycanvas').getContext('2d');  // set canvas' context variable
draw({
		red:                       // line name
		{ color: "#FF0000",        // set line color
				x: [0.0, 5.0],     // set x coordinates
				y: [0.0, 5.0],     // set y coordinates
		},
	},
	context,  // canvas' context
	0,        // points' circle radius
	1,        // line width
	false     // fill color
);
```

##Basic Usage — Multiple lines at once
```javascript
var context = document.getElementById('mycanvas').getContext('2d');  // set canvas' context variable
draw({
		black:                     // line name
		{ color: "#000000",        // set line color
				x: [0.0, 5.0],     // set x coordinates
				y: [0.0, 5.0],     // set y coordinates
		},
		blue:                      // line name
		{ color: "#0000FF",        // set line color
				x: [5.0, 0.0],     // set x coordinates
				y: [5.0, 5.0],     // set y coordinates
		},
		// add any amount of lines here
	},
	context,  // canvas' context
	0,        // points' circle radius
	1,        // line width
	false     // fill color
);
```

##Basic Usage — Multiple lines seperately
```javascript
var context = document.getElementById('mycanvas').getContext('2d');  // set canvas' context variable
draw({
		black:                     // line name
		{ color: "#000000",        // set line color
				x: [0.0, 5.0],     // set x coordinates
				y: [0.0, 5.0],     // set y coordinates
		},
	},
	context,  // canvas' context
	0,        // points' circle radius
	1,        // line width
	false     // fill color
);
draw({
		blue:                      // line name
		{ color: "#0000FF",        // set line color
				x: [5.0, 0.0],     // set x coordinates
				y: [5.0, 5.0],     // set y coordinates
		},
	},
	context,  // canvas' context
	0,        // points' circle radius
	1,        // line width
	false     // fill color
);
```

##Basic Usage — Filling between lines
```javascript
draw({
		black:                     // line name
		{ color: "#000000",        // set line color
		// make a full loop starting and ending
		// with the same coordinates
				x: [0.0, 5.0, 5.0, 0.0],     // set x coordinates
				y: [0.0, 5.0, 0.0, 0.0],     // set y coordinates
		},
	},
	context,  // canvas' context
	0,        // points' circle radius
	1,        // line width
	// set a color to fill between
	// all of the connected lines
	false     // fill color
);
```