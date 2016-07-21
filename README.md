node-yourls - Yourls API for nodejs
====================

This module provides hooks into the [Yourls](http://yourls.org/) API for [Nodejs](http://nodejs.org).
For more information about Yourls and what it can do, visit their [API docs](http://yourls.org/#API).

Note
----
YOURLS is a small set of PHP scripts that will allow you to run your own URL shortening service (a la TinyURL). You can make it private or public, you can pick custom keyword URLs.  This means you will need the URL of your, or someone else's, YOURLS installation as well as an API Signature token for that install.

Works over both http and https.

This module was originally written by Gabriel Preston. I cloned and modified from [node-yourls](https://github.com/gabrielpreston/node-yourls) to add minor additional feature on `shorten` funcionality for personal use.


Installation
------------
**with Node.js**

`yourls.js` is available on [NPM](https://www.npmjs.org/package/node-yourls)

You can install it with the following command:

    npm install node-yourls

Usage
-----
	var Yourls = require('./node-yourls/yourls');

	var yourls_url = 'ph.ly';
	var yourls_api = '1a40d1e654';

	var yourls = new Yourls(yourls_url, yourls_api);

	yourls.shorten('https://github.com/nandarustam/node-yourls', 'title', function(error, result) {
		if (error) {
			throw error;
		}
		console.log(result);
	});


Tests
-----
To run tests type `npm test`

Yourls Features
---------------
* shorten
* vanity
* expand
* urlstats
* stats
* dbstats