node-profanity-middleware
=========================

A foul-language filter for NodeJS that works seamlessly as a middleware

## Installation

  npm install profanity-middleware --save

## Usage

*As middleware with Express:*
	var app = express();
	var profanity = require('profanity-middleware');
	app.use(profanity.init); //will filter all user input data in all routes

*As function:*

  var profanity = require('profanity-middleware')
      filter = profanity.filter;

  var html = '<h1>Hello Foul World</h1>',
      filtered = filter(html, {blacklist: ['foul']});

  console.log('html', html, 'filtered', filtered);

## Tests

  npm test

## Contributing

In lieu of a formal styleguide, take care to maintain the existing coding style.
Add unit tests for any new or changed functionality. Lint and test your code.

## Release History

* 0.1.0 Initial release