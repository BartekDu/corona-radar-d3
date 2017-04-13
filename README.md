this version loads nested data from data.json:

index.html

//Load the data and Call function to draw the Radar chart
d3.json("data.json", function(error, data){
	RadarChart(".radarChart", data, radarChartOptions);
});
then, it converts the nested data into an array of values arrays:

radarChart.js

// convert the nested data passed in
// into an array of values arrays
data = data.map(function(d) { return d.values })
an iteration on the bl.ock Radar Chart Redesign created by @nbremer

forked from micahstubbs's block: radar chart for nested data

https://gist.github.com/micahstubbs/44bb05aab218a40a4c12

# \<corona-radar\>



## Install the Polymer-CLI

First, make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. Then run `polymer serve` to serve your application locally.

## Viewing Your Application

```
$ polymer serve
```

## Building Your Application

```
$ polymer build
```

This will create a `build/` folder with `bundled/` and `unbundled/` sub-folders
containing a bundled (Vulcanized) and unbundled builds, both run through HTML,
CSS, and JS optimizers.

You can serve the built versions by giving `polymer serve` a folder to serve
from:

```
$ polymer serve build/bundled
```

## Running Tests

```
$ polymer test
```

Your application is already set up to be tested via [web-component-tester](https://github.com/Polymer/web-component-tester). Run `polymer test` to run your application's test suite locally.
