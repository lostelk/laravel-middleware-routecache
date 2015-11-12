## Laravel Page Cache Use Middleware

###Installation
Add to composer.json

```php
"sid/laravel-simplecache-middleware":"dev-master"
```


Register the service provider by adding in the provider section in config/app.php

```php
'providers' => [
    ...
    Sid\SimpleCache\SimpleCacheServiceProvider::class
    ...
```

Just in case

```php
composer dump-autoload
```

Publish the migration and the config file

```php
php artisan vendor:publish
```

Add to Kernel.php

```php
'cacheafter' => \Sid\SimpleCache\AfterCacheMiddleware::class,
'cachebefore' => \Sid\SimpleCache\BeforeCacheMiddleware::class,
```