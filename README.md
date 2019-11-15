# Lumen PHP Framework

## Installation 
### Via Lumen Installer (run the following command)
```
composer global require "laravel/lumen-installer"
lumen new BlogApi
```
### Via Composer 
> composer create-project --prefer-dist laravel/lumen blog
## Run the development server
> php -S localhost:8000 -t public
## Configuration
### Application Key
From Laravel Lumen 6.x, you can now do this
on your routes/web.php file, add these lines temporarily
```php
use Illuminate\Support\Str;

$router->get('/key', function() {
return Str::random(32);
});
```
Then go to /key in your browser and copy paste the key into your .env file. 
Afterwards remove the lines above from the route file.