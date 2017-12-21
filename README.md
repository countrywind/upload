# yii2-qiniu

[![Latest Version on Packagist][ico-version]][link-packagist]
[![Total Downloads][ico-downloads]][link-downloads]

=================================
* @author crazyfd <crazyfd@qq.com>

> 只是因为原作者没有发布正式版本，造成了在生产环境使用困难，所以fork一份自己发布成正式版

file upload for Yii Framework 2

php > 5.5 

How to install?
To use this extension, you may insert the following code:
--------------------------------

Get it via [composer](http://getcomposer.org/) by adding the package to your `composer.json`:

```shell
composer require miuhr/yii2-qiniu
```

Usage
-----

```php
<?php
$ak = 'sss';
$sk = 'sss';
$domain = 'http://demo.domain.com/';
$bucket = 'demo';
use crazyfd\qiniu\Qiniu;
$qiniu = new Qiniu($ak, $sk,$domain, $bucket);
$key = time();
$qiniu->uploadFile($_FILES['tmp_name'],$key);
$url = $qiniu->getLink($key);
```

[ico-version]: https://img.shields.io/packagist/v/miuhr/yii2-qiniu.svg
[link-packagist]: https://packagist.org/packages/miuhr/yii2-qiniu

[ico-downloads]: https://img.shields.io/packagist/dt/miuhr/yii2-qiniu.svg
[link-downloads]: https://packagist.org/packages/miuhr/yii2-qiniu
