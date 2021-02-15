# Middleware about CORS in Lumen/PHP

  - Only get the file and put in ´app/Http/Middleware`
  - To use, follow these steps:
    • uncomment these linrd in file `bootstrap/app.php`:
      ```php
        $app->withFacades();
        $app->withEloquent();
      ```
    • add in file `bootstrap/app.php` the code:
      ```php
        $app->middleware([
            App\Http\Middleware\CorsMiddleware::class
        ]);
      ```
    • if you want create routerMiddleware (to use in specific routes), you can add the code:
      ```php
        $app->routeMiddleware([
            'cors' => App\Http\Middleware\CorsMiddleware::class,
        ]);
      ```
