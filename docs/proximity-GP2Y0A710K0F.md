<!--remove-start-->

# Proximity - GP2Y0A710K0F

<!--remove-end-->


Basic infrared Proximity example with GP2Y0A710K0F sensor.





##### Breadboard for "Proximity - GP2Y0A710K0F"



![docs/breadboard/proximity-GP2Y0A710K0F.png](breadboard/proximity-GP2Y0A710K0F.png)<br>

Fritzing diagram: [docs/breadboard/proximity-GP2Y0A710K0F.fzz](breadboard/proximity-GP2Y0A710K0F.fzz)

&nbsp;




Run with:
```bash
node eg/proximity-GP2Y0A710K0F.js
```


```javascript
var five = require("johnny-five");
var board = new five.Board();

board.on("ready", function() {
  var proximity = new five.Proximity({
    controller: "GP2Y0A710K0F",
    pin: "A0"
  });

  proximity.on("data", function() {
    console.log(this.cm + "cm", this.in + "in");
  });

  proximity.on("change", function() {
    console.log("The obstruction has moved.");
  });
});

```








&nbsp;

<!--remove-start-->

## License
Copyright (c) 2012, 2013, 2014 Rick Waldron <waldron.rick@gmail.com>
Licensed under the MIT license.
Copyright (c) 2014, 2015 The Johnny-Five Contributors
Licensed under the MIT license.

<!--remove-end-->
