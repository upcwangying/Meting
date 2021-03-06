<p align="center">
<img src="https://user-images.githubusercontent.com/2666735/30165599-36623bea-93a6-11e7-8956-1ddf99ce0e6f.png" alt="Meting">
</p>

<p align="center">
<a href="https://i-meto.com"><img alt="Author" src="https://img.shields.io/badge/Author-METO-blue.svg?style=flat-square"/></a>
<a href="https://packagist.org/packages/metowolf/Meting"><img alt="Version" src="https://img.shields.io/packagist/v/metowolf/Meting.svg?style=flat-square"/></a>
<a href="https://packagist.org/packages/metowolf/meting/stats"><img alt="Downloads" src="https://img.shields.io/packagist/dt/metowolf/Meting.svg?style=flat-square"/></a>
<a href="https://travis-ci.org/metowolf/Meting"><img alt="Travis" src="https://img.shields.io/travis/metowolf/Meting.svg?style=flat-square"></a>
<img alt="License" src="https://img.shields.io/packagist/l/metowolf/Meting.svg?style=flat-square"/>
</p>

 > :cake: Wow, such a powerful music API framework

## Introduction
A powerful music API framework to accelerate development

 + **Easy** - Easy to use, suppose format return.
 + **Light** - 42KB around with only one file.
 + **Powerful** - Suppose various webserver, include tencent, netease, xiami, kugou, baidu and more.
 + **Free** - Under MIT license, you can use it anywhere if you want.

## Requirement
PHP 5.4+ and BCMath, Curl, OpenSSL extension installed

## Install
Require this package, with [Composer](https://getcomposer.org), in the root directory of your project.

```bash
$ composer require metowolf/meting
```

Then you can import the class into your application:

```php
use Metowolf\Meting;

$api = new Meting('tencent');

$data = $api->format(true)->search('Soldier');
```

> **Note:** Meting requires the [BCMath](http://php.net/manual/en/book.bc.php), [cURL](http://php.net/manual/en/book.curl.php) and [OpenSSL](http://php.net/manual/en/book.openssl.php) extension in order to work.


## Quick Start
```php
require 'vendor/autoload.php';
// require 'Meting.php';

use Metowolf\Meting;

// Initialize to tencent API
$api = new Meting('tencent');

// Use custom cookie (option)
// $api->cookie('paste your cookie');

// Get data
$data = $api->format(true)->search('Soldier', [
    'page' => 1,
    'limit' => 50
]);

echo $data;
// [{"id":"0036bJCO3iRu9h","name":"Soldier","artist":["Samantha Jade"],"album":"Soldier","pic_id":"004GeOXp2mmIV7","url_id":"0036bJCO3iRu9h","lyric_id":"0036bJCO3iRu9h","source":"tencent"},{...},{...},...]

// Parse link
$data = $api->format(true)->url();

echo $data;
// {"url":"https://...","size":11823019,"br":320}
```

## More usage
 - [docs](https://github.com/metowolf/Meting/wiki)
 - [special for netease](https://github.com/metowolf/Meting/wiki/special-for-netease)

## Join the Discussion
 - [Telegram Group](https://t.me/adplayer)
 - [Official website](https://i-meto.com)

## Related Projects
 - [Hermit-X (Wordpress)](https://github.com/MoePlayer/Hermit-X)
 - [APlayer-Typecho](https://github.com/MoePlayer/APlayer-Typecho)
 - [MKOnlineMusicPlayer](https://github.com/mengkunsoft/MKOnlineMusicPlayer)
 - [WP-Player](https://github.com/webjyh/WP-Player)

## Author

**Meting** © [metowolf](https://github.com/metowolf), Released under the [MIT](./LICENSE) License.<br>

> Blog [@meto](https://i-meto.com) · GitHub [@metowolf](https://github.com/metowolf) · Twitter [@metowolf](https://twitter.com/metowolf) · Telegram Channel [@metooooo](https://t.me/metooooo)
