# Working Request Data

## Getting values dynamics
```php
$route->get('/sport/{something}', function($request) {
     echo $request->getUrlBodyWith('something');
});
```

## Getting all values dynamics
```php
$route->get('/sport/{something}/{name}', function($request) {
     var_dump($request->getUrlBodyAll());
});
```

## Getting specific query
```php
// /person?age=20
$route->get('/person', function($request) {
     var_dump($request->getQueryWith('status));
});
```

## Getting all queries
```php
// /person?age=20&name=Erandir
$route->get('/person', function($request) {
     var_dump($request->getQueryAll());
});
```

## Getting request body
```php
$route->post('/people', function($request) {
     echo $request->getUrlBodyWith('id');
});
```

## Getting all request body
```php
$route->put('/people', function($request) {
     var_dump($request->all());
});
```

## Getting files sended
```php
$route->post('/people', function($request) {
     var_dump($request->getUploadFiles());
});
```

## Getting type request
```php
$route->post('/people', function($request) {
     echo $request->getMethod();
});
```

[Response](response.md)