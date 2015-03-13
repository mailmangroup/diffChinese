diffChinese
===========

## Introduction
This module comparea two strings and outputs the differences.

It is based on, and borrows heavily from, John Resig's Javascript Diff Algorithm (http://ejohn.org/projects/javascript-diff-algorithm/). Thanks, John!

The main difference is that this module supports finding differences in strings containing Chinese or other languages that use multi byte characters and/or don't separate words by spaces.

Here is how the [KAWO.com](http://kawo.com) app uses this package: 

![Usage example.](diff-example.png)


## Installation

```bash
$ bower install diffChinese
```

## Including diffChinese

### RequireJS (recommended)
```javascript
require.config({
	paths: {
		diffChinese: '../bower_components/diffChinese/dist/diffChinese'
	}
});

require( [ 'diffChinese' ], function( diffChinese ) {
	...
});

```

### Basic Script Include
```html
<script src="./bower-components/diffString/dist/diffString.min.js"></script>
<script>
...
</script>
```

## Usage

The **diffChinese** package contains only one function `diffChinese` which can be used like this:
```javascript
var beforeString = 'the quick brown fox';
var afterString = 'the quick brown dog';

var diff = diffChinese( beforeString, afterString );

// => { before: 'the quick brown <del>fox</del>', after: 'the quick brown <ins>fox</ins>' }
```