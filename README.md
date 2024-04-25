Kohana Image for Yii 2
=====
Image manipulations (resize, crop, watermark, etc)

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist ybsisgood/image "*"
```

or add

```
"ybsisgood/image": "*"
```

to the require section of your `composer.json` file.

Configuration
-------------

In your config/web.php

```php
	'modules'=>[
		...

		'migrations'=>[
			'class'=>'ybsisgood\modules\migrations\MigrationModule'
		],

		...
	],
```

In you config/console.php

```php
	...

	'controllerMap'=>[
		'migrate'=>[
			'class'=>'ybsisgood\modules\migrations\components\MigrateController',
		],
	],

	...
```

Include your desired modules in config/console.php

Usage
-----

```php
\ybsisgood\image\Image::factory($pathFromFile)->resize(500, 300)->save($pathToFile);
```