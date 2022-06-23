-> php artisan make:model -a -r <name of model>
    -a : creates model, database migration, factory and controller
    -r : makes a resource controller
    make the controllers name plural
-> php artisan make:resource <resource name>
-> php artisan make:request <RequestName> ( ex AuthorsRequest )

-> Route::apiResource('/{route}',{controller}::class);
    creates all the routes for that controller 
    
    -> Controller's index => public function index()
    {
        return AuthorsResource::collection(Author::all());
    }
    
    
-> POST method => in StoreAuthorRequest.php change the return value of authorize function to true. Its default is false
