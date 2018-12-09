# CakePHP Mailgun Transport

Allows sending emails via Mailgun by using the provided SDK.

Supports email parameters listed in http://documentation.mailgun.com/api-sending.html#sending.

## Requirements

* PHP 5.6 or later
* Composer
* CakePHP 2.x

## Installation

* Install with composer by running `composer require silphroad/cakephp-mailgun`
* Include the plugin in your bootstrap's `CakePlugin::load('Mailgun')` or `CakePlugin::loadAll()`
* Configure Mailgun service

## Example of configuration

```php
<?php

class EmailConfig {

    public $mailgun = array(
        'transport'  => 'Mailgun.Mailgun',
        'domain'     => 'my-domain.mailgun.org',
        'api_key'    => 'my-mailgun-key'
        'from'       => array('no-reply@my-app.com' => 'My App'),

        // Custom mailgun settings, e.g.:
        'o:tag'      => 'tag1',
        'o:campaign' => 'my-campaign',
    );
}
```
