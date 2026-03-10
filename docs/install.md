# Installation

This page contains information about installing the Appning API Client Library for PHP.

## Requirements

* [PHP 8.1 or higher](https://www.php.net/)

## Obtaining the client library

### Composer (recommended)

The preferred method is via [Composer](https://getcomposer.org/). Follow the [installation instructions](https://getcomposer.org/doc/00-intro.md) if you do not already have Composer installed.

Once Composer is installed, run the following in your project root:

```sh
composer require appning/apiclient
```

If you encounter a timeout, increase Composer’s process timeout, for example:

```sh
COMPOSER_PROCESS_TIMEOUT=600 composer require appning/apiclient
```

Or add this to the `config` section of your `composer.json`:

```json
{
    "config": {
        "process-timeout": 600
    }
}
```

### Include the autoloader

After installing, include the autoloader in your application:

```php
require_once '/path/to/your-project/vendor/autoload.php';
```

### Dependency on `google/apiclient-services`

This library depends on `google/apiclient-services`, which provides the API wrappers. The client does not pin a specific version of that package so you can use the latest API clients. **To avoid breaking changes in production**, it is recommended that you pin to the [latest version](https://github.com/googleapis/google-api-php-client-services/releases) of `google/apiclient-services` in your own `composer.json` before going to production.

For more details, examples, and authentication (JWT Bearer / Appning), see the [main README](../README.md).
