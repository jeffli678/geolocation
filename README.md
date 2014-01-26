Geolocation
===========

A PHP library to query [Mozilla's][] or [Google's][] location service for
geolocation lookup based on the visible cell tower or wifi access points.

How to use
----------

	include_once('src/mozillageolocation.php');

	$m = new MozillaGeolocation('your_api_key_here');

	$wifis = array("00:11:22:33:44:55", ... visible BSSIDs here ...);

	$location = $m->getCoordinates($wifis);

`$location` is now either a location (array):

	{
		"location": {
			"lat": 51.0,
			"lng": -0.1
		},
		"accuracy": 1200.4
	}

or an [error description][] (string).

License
-------

The MIT License (MIT)

Copyright (c) 2014 Morris Jobke

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

[Mozilla's]: https://location.services.mozilla.com/
[Google's]: https://developers.google.com/maps/documentation/business/geolocation/
[error description]: https://developers.google.com/maps/documentation/business/geolocation/#errors