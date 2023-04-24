# Simple class sessions with functions has, set, destroy, unset and others.


## Installation

Session is available via Composer:

```bash
"brdev/sessions": "1.0"
```

or run

```bash
composer require brdev/sessions
```

## EXAMPLES THE WITH USE

```php

<?php

use BRdev\Sessions\Session;

require __DIR__."/../vendor/autoload.php";

$session = new Session(__DIR__."/sessions/");

if(false){
    //SESSION REGENERATE
    $session->regenerate();
}

if(false){
    //SET KEY
    $session->set("name","luciano");

    //GET SESSION
    echo $session->name;
}


if(false){
    //HAS KEY
    if($session->has("name")){
        echo $session->name;
        return;
    }

    $session->set("name","luciano");
    //GET SESSION
    echo $session->name;
}

if(false){
    //HAS KEY
    if($session->has("name")){
        echo $session->name;
    }
}

if(false){
    //SESSION DESTROY
    $session->destroy();
}

if(false){
    //SESSION DELETE SET
    $session->unset("name");
}

if(true)
{
    //SESSION CSRF
    $session->csrf();
    echo $session->csrf_token;
}

```
