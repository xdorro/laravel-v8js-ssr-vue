# Server side rendering JavaScript with Vuejs in your Laravel application

## Installation

**1** Composer
```command
    composer install
```

**2** Yarn
```command
    yarn install
```

**3** add config your webpack.mix.js below

```javascript
mix.js("resources/js/client.js", "public/js")
    .js("resources/js/server.js", "public/js")
    .sass("resources/sass/app.scss", "public/css");
```

This package will create component `AppSSR.vue` `AppSSR.js` `client.js` `server.js` `ssr.blade.php`

**4** Development
```command
    yarn development
```

**5** Production
```command
    yarn production
```

**6** please change or remove some routes like '/' in `routes/web.php`

Example:

```php
Route::get('/', function () { // change '/' to '/something'
    return view('welcome');
});
```

now you can go yourdomain and view page source have `data-server-rendered="true"`
