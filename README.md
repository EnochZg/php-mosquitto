# yii2-mosquitto

## Installation

The component is based on `php-mosquitto` extension. The download link is `https://github.com/mgdm/Mosquitto-PHP`.

```bash
composer require enochzg/yii2-mosquitto
```

## Usage

Add target class in your project config:

```php
'components' => [
    'mosquitto' => [
        'class' => 'enochzg\mosquitto\Mosquitto',
        'host' => '127.0.0.1',
        'port' => '1883',
        'keepalive' => 60,
        'cafile' => '[your/cert/path]/ca.crt',
        'certfile' => '[your/cert/path]/client.crt',
        'keyfile' => '[your/cert/path]/client.key',
    ],
    //......
]
```

e.g.
```php
yii::$app->mosquitto->publish('1', 'message', 2);
```