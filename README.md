#deprecations <sup>[![Version Badge][2]][1]</sup>

[![Build Status][3]][4] [![dependency status][5]][6] [![dev dependency status][7]][8]

[![npm badge][9]][1]

Given an npm module name, get a map of npm version numbers to deprecation messages.

## Example
```js
var deprecations = require('deprecations');
var messages = deprecations('forms', 'object.assign');
var assert = require('assert');
assert.deepEqual(messages, {
	forms: {
		'0.1.0': 'Please update to the latest version',
		'0.1.1': 'Please update to the latest version',
		'0.1.2': 'Please update to the latest version',
		'0.1.3': 'Please update to the latest version',
		'0.1.4': 'Please update to the latest version',
		'0.2.0': 'Please update to the latest version',
		'0.2.1': 'Please update to the latest version',
		'0.2.2': 'Please update to the latest version',
		'0.2.3': 'Please update to the latest version',
		'0.3.0': 'Please update to the latest version',
		'0.4.0': 'Please update to the latest version',
		'0.4.1': undefined
	},
	'object.assign': {
		'0.1.0': 'Please upgrade to the latest spec-compliant version',
		'0.1.1': 'Please upgrade to the latest spec-compliant version',
		'0.2.0': 'Please upgrade to the latest spec-compliant version',
		'0.2.1': 'Please upgrade to the latest spec-compliant version',
		'0.3.1': undefined
	}
});
```
## Tests
Simply clone the repo, `npm install`, and run `npm test`

[1]: https://npmjs.org/package/deprecations
[2]: http://vb.teelaun.ch/ljharb/npm-deprecations.svg
[3]: https://travis-ci.org/ljharb/npm-deprecations.png
[4]: https://travis-ci.org/ljharb/npm-deprecations
[5]: https://david-dm.org/ljharb/npm-deprecations.png
[6]: https://david-dm.org/ljharb/npm-deprecations
[7]: https://david-dm.org/ljharb/npm-deprecations/dev-status.png
[8]: https://david-dm.org/ljharb/npm-deprecations#info=devDependencies
[9]: https://nodei.co/npm/deprecations.png?downloads=true&stars=true

