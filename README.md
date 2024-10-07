# Mailcow PHP API Client

# Getting Started
### Requirements
* [**PHP 7.2+**](https://www.php.net/downloads.php)
* Extensions: [Composer](https://getcomposer.org/), [PHP-JSON](https://www.php.net/manual/en/book.json.php)

In the root of your project execute the following:
```sh
$ composer require mscode-pl/mailcow-php-api
```
or add this to your `composer.json` file:
```json
{
    "require": {
        "mscode-pl/mailcow-php-api": "^0.14.1"
    }
}
```

Then perform the installation:
```sh
$ composer install --no-dev
```

# Usage

Search for the API Documentation [here](https://mailcow.docs.apiary.io/).  
You need an API Key for that.

### Example

```php
<?php
// Require the autoloader
require_once 'vendor/autoload.php';

// Use the library namespace
use MsCode\Mailcow\MailCowAPI;

// Then simply pass your API-Token when creating the API client object.
$client = new MailCowAPI('mailcow-with-https.example.com','MAILCOW_API_KEY');

// Then you are able to perform a request
var_dump($client->domains()->getDomains());
?>
```
