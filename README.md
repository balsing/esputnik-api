# PHP ESputnik API клиент

Uses [Esputnik API](https://esputnik.com.ua/api/index.html).


## Требования

* PHP >= 5.6
* [Guzzle 6.0+](https://github.com/guzzle/guzzle) library,
* (optional) PHPUnit to run tests.

## Установка
1. Добавить в секцию ``repositories``:
{
    "type": "git",
    "url": "ssh://git@git.crtweb.ru:22681/youtool/esputnik-api.git"
}

2. Выполнить команду 

```
composer require youtool/esputnik-api-client
```


## Basic usage

```php
<?php

require_once 'vendor/autoload.php';

$client = new \Esputnik\Client();
$client->authenticate('login', 'password');

$repositories = $client->api('balance')->show();
```

From `$client` object, you can access to all namespaces.

## Inspired by

[n10ty/php-esputnik-api](https://github.com/n10ty/php-esputnik-api)

## License

MIT License
