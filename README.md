### Lazada PHP SDK

Why ?

- Lazada official SDK is bad code (no tests, raw CURL implementations, no packagist package)
- Has 1 error (LazopClient line 114, "no varriable named reponse")
- Remove default error handler so developer can assigned new error handler he want

```php
$client = LazopClient(....)
$client->errorHandler = function($requestUrl, $errorCode, $responseTxt) {
    // implement your error handler here
};
```

NO GUARANTEE !!! I just fixed what I can !
