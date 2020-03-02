# PHP ESputnik API клиент

Uses [Esputnik API](https://esputnik.com.ua/api/index.html).


## Требования

* PHP >= 5.6
* [Guzzle 6.0+](https://github.com/guzzle/guzzle) library,
* (optional) PHPUnit to run tests.

## Установка
1. Добавить в секцию ``repositories``:
```
{
    "type": "git",
    "url": "https://github.com/balsing/esputnik-api-library.git"
}
```

2. Выполнить команду 

```
composer require balsing/esputnik-api-library
```


## Использование

```php
<?php

require_once 'vendor/autoload.php';

$client = new \Esputnik\Client();
$client->authenticate('login', 'password');

$repositories = $client->api('balance')->show();
```

From `$client` object, you can access to all namespaces.

## Создан на основе

[n10ty/php-esputnik-api](https://github.com/n10ty/php-esputnik-api)

## Лицензия

MIT License
