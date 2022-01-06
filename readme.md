[//]: # (header-start)

<a href="https://brenton.house/saying-goodbye-to-axway-amplify-titanium-31a44f3671de">
	<h1 align="center">
	🪦 RIP Axway Amplify Titanium (2010 - 2022)
	</h1>
</a>
<a href="https://brenton.house/saying-goodbye-to-axway-amplify-titanium-31a44f3671de">
	<p align="center">
		<img src="https://cdn.secure-api.org/images/RIP-Axway-Amplify-Titanium.png" alt="RIP Axway Amplify Titanium (2010 - 2022)" width="80%" />
	</p>
</a>
<a href="https://brenton.house/saying-goodbye-to-axway-amplify-titanium-31a44f3671de">
	<p align="center">
		🪦 &nbsp; RIP Axway Amplify Titanium (2010 - 2022)
	</p>
</a>
<p>&nbsp;</p>
<a href="https://brenton.house/saying-goodbye-to-axway-amplify-titanium-31a44f3671de">
	<h2 align="center">
		🛑 This project is no longer being maintained 🛑
	</h2>
</a>
<p>&nbsp;</p>
<hr>
<p>&nbsp;</p>
<p>&nbsp;</p>

[//]: # (header-end)


# @titanium/json5

[![@titanium/json5](https://img.shields.io/npm/v/@titanium/json5.png)](https://www.npmjs.com/package/@titanium/json5)
[![Dependabot Status](https://api.dependabot.com/badges/status?host=github&repo=brentonhouse/titanium-lottie)](https://dependabot.com)


> Titanium native mobile module for JSON5 - JSON for Humans.  Based on https://github.com/json5/json5 


* [📝 Description](#-description)
	* [JSON5 – JSON for Humans](#json5--json-for-humans)
* [🚀 Getting Started](#-getting-started)
* [Usage](#usage)
	* [Short Example](#short-example)
* [Features](#features)
	* [Objects](#objects)
	* [Arrays](#arrays)
	* [Strings](#strings)
	* [Numbers](#numbers)
	* [Comments](#comments)
	* [White Space](#white-space)
* [API](#api)
	* [JSON5.parse()](#json5parse)
		* [Syntax](#syntax)
		* [Parameters](#parameters)
		* [Return value](#return-value)
	* [JSON5.stringify()](#json5stringify)
		* [Syntax](#syntax-1)
		* [Parameters](#parameters-1)
		* [Return value](#return-value-1)
	* [Node.js `require()` JSON5 files](#nodejs-require-json5-files)
* [🔗 Related Links](#-related-links)
* [📚 Learn More](#-learn-more)
* [📣 Feedback](#-feedback)
* [©️ Legal](#️-legal)
	* [License](#license)
	* [Credits](#credits)

## 📝 Description

### JSON5 – JSON for Humans

The JSON5 Data Interchange Format (JSON5) is a superset of [JSON] that aims to
alleviate some of the limitations of JSON by expanding its syntax to include
some productions from [ECMAScript 5.1].

## 🚀 Getting Started

Install using npm:

```
npm install @titanium/json5
```

## Usage

 ```javascript
const JSON5 = require('@titanium/json5');  // or use require('json5');
JSON5.parse();
JSON5.stringify();
 ```

### Short Example
```js
{
  // comments
  unquoted: 'and you can quote me on that',
  singleQuotes: 'I can use "double quotes" here',
  lineBreaks: "Look, Mom! \
No \\n's!",
  hexadecimal: 0xdecaf,
  leadingDecimalPoint: .8675309, andTrailing: 8675309.,
  positiveSign: +1,
  trailingComma: 'in objects', andIn: ['arrays',],
  "backwardsCompatible": "with JSON",
}
```


## Features

The following ECMAScript 5.1 features, which are not supported in JSON, have
been extended to JSON5.

### Objects
- Object keys may be an ECMAScript 5.1 _[IdentifierName]_.
- Objects may have a single trailing comma.

### Arrays
- Arrays may have a single trailing comma.

### Strings
- Strings may be single quoted.
- Strings may span multiple lines by escaping new line characters.
- Strings may include character escapes.

### Numbers
- Numbers may be hexadecimal.
- Numbers may have a leading or trailing decimal point.
- Numbers may be [IEEE 754] positive infinity, negative infinity, and NaN.
- Numbers may begin with an explicit plus sign.

### Comments
- Single and multi-line comments are allowed.

### White Space
- Additional white space characters are allowed.

[IdentifierName]: https://www.ecma-international.org/ecma-262/5.1/#sec-7.6

[IEEE 754]: http://ieeexplore.ieee.org/servlet/opac?punumber=4610933


## API
The JSON5 API is compatible with the [JSON API].

[JSON API]:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON

### JSON5.parse()
Parses a JSON5 string, constructing the JavaScript value or object described by
the string. An optional reviver function can be provided to perform a
transformation on the resulting object before it is returned.

#### Syntax
    JSON5.parse(text[, reviver])

#### Parameters
- `text`: The string to parse as JSON5.
- `reviver`: If a function, this prescribes how the value originally produced by
  parsing is transformed, before being returned.

#### Return value
The object corresponding to the given JSON5 text.

### JSON5.stringify()
Converts a JavaScript value to a JSON5 string, optionally replacing values if a
replacer function is specified, or optionally including only the specified
properties if a replacer array is specified.

#### Syntax
    JSON5.stringify(value[, replacer[, space]])
    JSON5.stringify(value[, options])

#### Parameters
- `value`: The value to convert to a JSON5 string.
- `replacer`: A function that alters the behavior of the stringification
  process, or an array of String and Number objects that serve as a whitelist
  for selecting/filtering the properties of the value object to be included in
  the JSON5 string. If this value is null or not provided, all properties of the
  object are included in the resulting JSON5 string.
- `space`: A String or Number object that's used to insert white space into the
  output JSON5 string for readability purposes. If this is a Number, it
  indicates the number of space characters to use as white space; this number is
  capped at 10 (if it is greater, the value is just 10). Values less than 1
  indicate that no space should be used. If this is a String, the string (or the
  first 10 characters of the string, if it's longer than that) is used as white
  space. If this parameter is not provided (or is null), no white space is used.
  If white space is used, trailing commas will be used in objects and arrays.
- `options`: An object with the following properties:
  - `replacer`: Same as the `replacer` parameter.
  - `space`: Same as the `space` parameter.
  - `quote`: A String representing the quote character to use when serializing
    strings.

#### Return value
A JSON5 string representing the value.

### Node.js `require()` JSON5 files
When using Node.js, you can `require()` JSON5 files by adding the following
statement.

```js
require('json5/lib/register')
```

Then you can load a JSON5 file with a Node.js `require()` statement. For
example:

```js
const config = require('./config.json5')
```



## 🔗 Related Links

- [Titanium Mobile](https://www.npmjs.com/package/titanium) - Open-source tool for building powerful, cross-platform native apps with JavaScript.
- [Alloy](https://www.npmjs.com/package/alloy) - MVC framework built on top of Titanium Mobile.
- [Appcelerator](https://www.npmjs.com/package/appcelerator) - Installer for the Appcelerator Platform tool
- [JSON5](https://www.json5.org) - JSON5 Home Page

## 📚 Learn More

- [Axway Developer Portal](https://developer.axway.com)

## 📣 Feedback

Have an idea or a comment?  [Join in the conversation here](https://github.com/brentonhouse/titanium-json5/issues)! 

## ©️ Legal

### License
MIT. See [license.md](./license.md) for details.

### Credits
[Assem Kishore](https://github.com/aseemk) founded this project.

[Michael Bolin](http://bolinfest.com/) independently arrived at and published
some of these same ideas with awesome explanations and detail. Recommended
reading: [Suggested Improvements to JSON](http://bolinfest.com/essays/json.html)

[Douglas Crockford](http://www.crockford.com/) of course designed and built
JSON, but his state machine diagrams on the [JSON website](http://json.org/), as
cheesy as it may sound, gave us motivation and confidence that building a new
parser to implement these ideas was within reach! The original
implementation of JSON5 was also modeled directly off of Doug’s open-source
[json_parse.js] parser. We’re grateful for that clean and well-documented
code.

[json_parse.js]:
https://github.com/douglascrockford/JSON-js/blob/master/json_parse.js

[Max Nanasy](https://github.com/MaxNanasy) has been an early and prolific
supporter, contributing multiple patches and ideas.

[Andrew Eisenberg](https://github.com/aeisenberg) contributed the original
`stringify` method.

[Jordan Tucker](https://github.com/jordanbtucker) has aligned JSON5 more closely
with ES5, wrote the official JSON5 specification, completely rewrote the
codebase from the ground up, and is actively maintaining this project.

Alloy is developed by Appcelerator and the community and is Copyright © 2012-Present by Appcelerator, Inc. All Rights Reserved.

Alloy is made available under the Apache Public License, version 2. See their license file for more information.

Appcelerator is a registered trademark of Appcelerator, Inc. Titanium is a registered trademark of Appcelerator, Inc. Please see the LEGAL information about using trademarks, privacy policy, terms of usage and other legal information at http://www.appcelerator.com/legal.