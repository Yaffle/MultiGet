
MultiGet
========

Simultaneuos HTTP requests with curl_multi and PHP 5.3+

```php
$mget = new MultiGet();
$mget->request('http://ya.ru')
->on('success', function ($content) {
  // this anonymous function will be called after request is loaded
  // so you can process data before all other downloads ends
  // also you can add new requests from here
});
$mget->go();// waits for downloads and executes callbacks
// at this point all work done...
```

Example
-------

see example.php

