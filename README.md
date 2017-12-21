yii2-qiniu
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
