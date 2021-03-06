[ci-img]: https://img.shields.io/travis/ciena-frost/ember-frost-fields.svg "Travis CI Build Status"
[ci-url]: https://travis-ci.org/ciena-frost/ember-frost-fields

[cov-img]: https://img.shields.io/coveralls/ciena-frost/ember-frost-fields.svg "Coveralls Code Coverage"
[cov-url]: https://coveralls.io/github/ciena-frost/ember-frost-fields

[npm-img]: https://img.shields.io/npm/v/ember-frost-fields.svg "NPM Version"
[npm-url]: https://www.npmjs.com/package/ember-frost-fields

[ember-observer-badge]: http://emberobserver.com/badges/ember-frost-fields.svg "Ember Observer score"
[ember-observer-badge-url]: http://emberobserver.com/addons/ember-frost-fields

[ember-img]: https://img.shields.io/badge/ember-2.3+-orange.svg "Ember 2.3+"

[bithound-img]: https://www.bithound.io/github/ciena-frost/ember-frost-fields/badges/score.svg "bitHound"
[bithound-url]: https://www.bithound.io/github/ciena-frost/ember-frost-fields

# ember-frost-fields

###### Dependencies

![Ember][ember-img]
[![NPM][npm-img]][npm-url]

###### Health

[![Travis][ci-img]][ci-url]
[![Coveralls][cov-img]][cov-url]

###### Security

[![bitHound][bithound-img]][bithound-url]

###### Ember Observer score
[![EmberObserver][ember-observer-badge]][ember-observer-badge-url]

## Overview
Ember-frost-fields provides different kinds of custom input fields and input areas.

### frost-url-input
Based on the [frost-text](http://ciena-frost.github.io/ember-frost-core/#/field) component
from [ember-frost-core](https://github.com/ciena-frost/ember-frost-core), the URL input
field consists of an input field and a button.
The component is used to verify that the provided URL is both valid and accessible.

After clicking the 'Test' button,
+ the entered URL is loosely verified to be correctly formatted.
+ An AJAX GET request is then sent (with JSONP to overcome cross-domain problems) to the destination URL.
+ The response is checked with any status code between 100 and 500, except 404, deemed a success.

Should MIME Checking be enabled and the Type set to 'Text', an error will be thrown when using the Chrome browser

## Testing with ember-hook

### frost-url-input
The file picker component is accessible using ember-hook with the top level hook name or you can access the internal
components as well -
* Default top level hook - `$hook('url-input')`
* Test button hook - `$hook('<hook-name>-button')`
* Input field hook - `$hook('<hook-name>-input')`

## Examples

API and example usage can be found in the sample application in tests/dummy, which is also running at http://ciena-frost.github.io/ember-frost-fields

### frost-url-input

```handlebars
{{frost-url-input}}
```

## Installation

* `git clone` this repository
* `npm install`
* `bower install`

## Running

* `ember server`
* Visit your app at http://localhost:4200.

## Running Tests

* `npm test` (Runs `ember try:testall` to test your addon against multiple Ember versions)
* `ember test`
* `ember test --server`
