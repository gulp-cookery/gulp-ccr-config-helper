# gulp-ccr-config-helper
Configuration helper functions. A cascading configurable gulp recipe for [gulp-chef](https://github.com/gulp-cookery/gulp-chef).

## Install

``` bash
$ npm install --save gulp-ccr-config-helper
```

## Usage

``` javascript
var verify = require('gulp-ccr-config-helper');

var schema = {
	title: 'my-plugin',
	description: 'my-plugin description',
	type: 'object'
	properties: {
		options: {
			type: 'object'
		}
	},
	required: ['options']
};

module.exports = function (done) {
    verify(schema, this.config);
	done();
};

module.exports.type = 'task';
```
