yii2-qiniu
=================================
* @author crazyfd <crazyfd@qq.com>

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
