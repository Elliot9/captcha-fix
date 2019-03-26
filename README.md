# captcha-fix
branch from mews for TTS 


Preview
-------
![img](https://i.imgur.com/PZe5UGm.png)

Download
-------
Require this package with composer:

composer require elliot9/captcha


Usage
-------
Find the providers key in config/app.php and register the Captcha Service Provider.

    'providers' => [
        // ...
        Elliot9\Captcha\CaptchaServiceProvider::class,
    ]
    
Find the aliases key in config/app.php.
 
    'aliases' => [
        // ...
        'Captcha' => Elliot9\Captcha\Facades\Captcha::class,
    ]
    
    
## Configuration
    php artisan vendor:publish
    config/captcha.php
    'default'   => [
        'length'    => 4,
        'width'     => 120,
        'height'    => 36,
        'quality'   => 90,
        'math'      => false,
        'account'   =>'', //TTS Account
        'password'  =>'', // TTS password
    ],
    
    
##Example Usage
    
    {{captcha_audio_src()}} => return Audio Captcha src
    {{captcha}} => Captcha img
