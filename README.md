Google Analytics Measurement Protocol library for PHP
===========================
[![Build Status](https://travis-ci.org/theiconic/php-ga-measurement-protocol.svg?branch=v1.0.1)](https://travis-ci.org/theiconic/php-ga-measurement-protocol) [![Coverage Status](https://img.shields.io/coveralls/theiconic/php-ga-measurement-protocol.svg)](https://coveralls.io/r/theiconic/php-ga-measurement-protocol?branch=master) [![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/theiconic/php-ga-measurement-protocol/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/theiconic/php-ga-measurement-protocol/?branch=master) [![Latest Stable Version](https://poser.pugx.org/theiconic/php-ga-measurement-protocol/v/stable.svg)](https://packagist.org/packages/theiconic/php-ga-measurement-protocol) [![Total Downloads](https://poser.pugx.org/theiconic/php-ga-measurement-protocol/downloads.svg)](https://packagist.org/packages/theiconic/php-ga-measurement-protocol) [![License](https://poser.pugx.org/theiconic/php-ga-measurement-protocol/license.svg)](https://packagist.org/packages/theiconic/php-ga-measurement-protocol) [![Documentation Status](https://readthedocs.org/projects/php-ga-measurement-protocol/badge/?version=latest)](http://php-ga-measurement-protocol.readthedocs.org/en/latest/)

## Description

Send data to Google Analytics from the server using PHP. This library fully implements GA measurement protocol so its possible to send any data that you would usually do from analytics.js on the client side. You can send data regarding the following parameters categories [(Full List)](https://developers.google.com/analytics/devguides/collection/protocol/v1/parameters):
* General
* User
* Session
* Traffic Sources
* System Info
* Hit
* Content Information
* App Tracking
* Event Tracking
* E-Commerce
* Enhanced E-Commerce
* Social Interactions
* Timing
* Exceptions
* Custom Dimensions / Metrics
* Content Experiments

## Usage
```php
use TheIconic\Tracking\GoogleAnalytics\Analytics;

// Instantiate the Analytics object
// optionally pass TRUE in the constructor if you want to connect using HTTPS
$analytics = new Analytics(true);

// Build the GA hit using the Analytics class methods
// they should autocomplete if you use a PHP IDE
$analytics
    ->setProtocolVersion('1')
    ->setTrackingId('UA-26293728-11')
    ->setClientId('12345678')
    ->setDocumentPath('/mypage');

// When you finish bulding the payload send a hit (such as an pageview or event)
$analytics->sendPageview();
```
The hit should have arrived to the GA property UA-26293728-11. You may verify this in your Real Time dashboard.

The library is 100% done, full documentation is a work in progress.

## Installation

Use Composer to install this package.

```json
{
    "require": {
        "theiconic/php-ga-measurement-protocol": "~1.0"
    }
}
```

## Contributors

* Jorge A. Borges - Lead Developer ([http://jorgeborges.me](http://jorgeborges.me))
* Juan Falcón - [arcticfalcon](https://github.com/arcticfalcon)

## License

THE ICONIC Google Analytics Measurement Protocol library for PHP is released under the MIT License.
