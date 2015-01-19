---
title: Get Started
template: documentation.twig::content_inner
chapter: 1
---

## Installation

- [Currency on Packagist](https://packagist.org/packages/torann/currency)
- [Currency on GitHub](https://github.com/torann/laravel-currency)

To get the latest version of Currency simply require it in your `composer.json` file.

~~~
"torann/currency": "dev-master"
~~~

You'll then need to run `composer install` to download it and have the autoloader updated.

Once Currency is installed you need to register the service provider with the application. Open up `app/config/app.php` and find the `providers` key.

~~~php
'providers' => array(
    'Torann\Currency\CurrencyServiceProvider',
)
~~~

Currency also ships with a facade which provides the static syntax for creating collections. You can register the facade in the `aliases` key of your `app/config/app.php` file.

~~~php
'aliases' => array(
    'Currency' => 'Torann\Currency\Facades\Currency',
)
~~~

Create configuration file using artisan

~~~
$ php artisan config:publish torann/currency
~~~

Generate the table by running

~~~
$ php artisan migrate --package=torann/currency
~~~