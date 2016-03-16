# yii2-mosquitto

## Installation

```bash
composer require enochzg/yii2-mosquitto
```

or add

```
"enochzg/yii2-mosquitto": "~1.0.0"
```

to the ```require``` section of your `composer.json` file.

## Usage

Add target class in your project config:

```php
<?php
'components' => [
    'mosquitto' => [
        'class' => 'enochzg\mosquitto\Mosquitto',
        'host' => '127.0.0.1',
    ],
    //......
]
?>
```

```php
<?php
    yii::$app->mosquitto->publish('1', 'message');
?>
```