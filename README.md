# hirestime [![Build Status](https://api.travis-ci.org/seriousManual/hirestime.png)](https://travis-ci.org/seriousmanual/hirestime)

...because there aren't enough hrtime wrappers yet.

[![NPM](https://nodei.co/npm/hirestime.png)](https://nodei.co/npm/hirestime/)

[![NPM](https://nodei.co/npm-dl/hirestime.png?months=3)](https://nodei.co/npm/hirestime/)

hirestime is a thin wrapper around `process.hrtime()` that does the clumsy handling of the returned array for you.

## Installation

````bash
npm install hirestime
````

## hirestime()
returns a function:

### returnedFunction([unit])
returns the elapsed time since the call of `hirestime` in milliseconds.    
an optional unit parameter can be specified that will cause an recalculation.    
possible parameters

* `hirestime.S` elapsed time in seconds
* `hirestime.MS` elapsed time in milliseoncds
* `hirestime.NS` elapsed time in nanoseconds

## Examples

````javascript
var hirestime = require('../');

//startpoint of the time measurement
var getElapsed = hirestime();

setTimeout(function() {
    //returns the elapsed milliseconds
    console.log(getElapsed());
}, 1000);
````
 
 ````javascript
var hirestime = require('../');

//startpoint of the time measurement
var getElapsed = hirestime();

setTimeout(function() {
    //returns the elapsed seconds
    console.log(getElapsed(hirestime.S));
}, 1000);
````
 
