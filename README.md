# NhiepPhong/Timthumb is Lib for Laravel PHP Framework
An image proxy for Laravel

[![Build Status](https://travis-ci.org/nhiepphong/timthumb.svg?branch=master)](https://travis-ci.org/nhiepphong/timthumb)
[![Latest Stable Version](https://poser.pugx.org/nhiepphong/timthumb/v/stable)](https://packagist.org/packages/nhiepphong/timthumb)
[![Total Downloads](https://poser.pugx.org/nhiepphong/timthumb/downloads)](https://packagist.org/packages/nhiepphong/timthumb)
[![Latest Unstable Version](https://poser.pugx.org/nhiepphong/timthumb/v/unstable)](https://packagist.org/packages/nhiepphong/timthumb)
[![License](https://poser.pugx.org/nhiepphong/timthumb/license)](https://packagist.org/packages/nhiepphong/timthumb)

default
## Installation
Run the following to include this via Composer

```shell
composer require nhiepphong/timthumb
```
and run composer update.

Once it's installed, you have to register the service provider. In `app/config/app.php` add the following line of code to the `providers` array:
```php
'nhiepphong\Timthumb\TimthumbServiceProvider'
```
If you want in `app/config/app.php` add the following line of code to the `alias` array
```php
'Timthumb' => 'nhiepphong\Timthumb\Facades\Timthumb'
```
Then, publish the config files with `php artisan config:publish nhiepphong/timthumb`.

Then, publish the asset files with `php artisan asset:publish nhiepphong/timthumb`.

## Usage
Generate the image link with the following line of code
```php
$url = Timthumb::link('path/to/image.jpg',width,height)
```
Set 0 width or 0 height to let Timthumb mantain the original image ratio
