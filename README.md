Forked from: https://github.com/marc-hughes/js-sha1

Two changes

1. Detects nodejs differently, so it works with webpack2 builds
2. Added optional parameter to get output as numeric array instead of hex string


# js-sha1
[![Build Status](https://travis-ci.org/marc-hughes/js-sha1.svg?branch=master)](https://travis-ci.org/marc-hughes/js-sha1)

A simple SHA1 hash function for JavaScript supports UTF-8 encoding.

## Demo
[SHA1 Online](http://emn178.github.io/online-tools/sha1.html)

## Download
[Compress](https://raw.github.com/emn178/js-sha1/master/build/sha1.min.js)  
[Uncompress](https://raw.github.com/emn178/js-sha1/master/src/sha1.js)

## Installation
You can also install js-sha1 by using Bower.

    bower install js-sha1

For node.js, you can use this command to install:

    npm install js-sha1

## Usage
You could use like this:
```JavaScript
sha1('Message to hash');
```
If you use node.js, you should require the module first:
```JavaScript
sha1 = require('js-sha1');
```

## Example
Code
```JavaScript
sha1('');
sha1('The quick brown fox jumps over the lazy dog');
sha1('The quick brown fox jumps over the lazy dog.');
```
Output

    da39a3ee5e6b4b0d3255bfef95601890afd80709
    2fd4e1c67a2d28fced849ee1bb76e7391b93eb12
    408d94384216f890ff7a0c3528e8bed1e0b01621

It also supports UTF-8 encoding:

Code
```JavaScript
sha1('中文');
```
Output

    7be2d2d20c106eee0836c9bc2b939890a78e8fb3

It also supports byte `Array`, `Uint8Array`, `ArrayBuffer` input:

Code
```JavaScript
sha1([]);
sha1(new Uint8Array([]));
```
Output

    da39a3ee5e6b4b0d3255bfef95601890afd80709
    da39a3ee5e6b4b0d3255bfef95601890afd80709

## Benchmark
[UTF8](http://jsperf.com/sha1-speed-test/11)  
[ASCII](http://jsperf.com/sha1-speed-test/10)

## Extensions
### jQuery
If you prefer jQuery style, you can add following code to add a jQuery extension.

Code
```JavaScript
jQuery.sha1 = sha1;
```
And then you could use like this:
```JavaScript
$.sha1('message');
```
### Prototype
If you prefer prototype style, you can add following code to add a prototype extension.

Code
```JavaScript
String.prototype.sha1 = function() {
  return sha1(this);
};
```
And then you could use like this:
```JavaScript
'message'.sha1();
```
## License
The project is released under the [MIT license](http://www.opensource.org/licenses/MIT).

## Contact
The project's website is located at https://github.com/emn178/js-sha1  
Author: emn178@gmail.com
