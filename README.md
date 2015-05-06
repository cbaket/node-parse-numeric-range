node-parse-numeric-range
========================

Parses expressions like 1-10,20-30. Returns an energetic (as opposed to lazy) array.


## Supported Expressions
Comprehensive supported expression examples:

| Expression | result       |
|:----------:|:------------:|
|            |   []         |
|     1      |   [1]        |
|    1,2     |  [1,2]       |
|    -10     |   []         |
|   -3,-3    |   []         |
|   -1-2,-2  |  [1,2]       |
|  -1--2     |   []         |
|  -1..2,-2  |  [1,2]       |
|  -1...3,-2 |  [1,2]       |


What's this useful for? Well, letting users input these sorts of things and then
making them programmatically useful.


## Usage

// not uploaded this version // First, `npm install parse-numeric-range`.
JUST require the module from index.js:
```javascript
var rangeParser = require('./index.js');

var nums = rangeParser.parse('4,6,8-10,12,14..16,18,20...23');

console.log("The first " + nums.length + " composite numbers are: " + nums.join(', ')); 
```
