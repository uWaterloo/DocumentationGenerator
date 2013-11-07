## API Documentation Generator


Given API method schema, the following class will generate a mardown documentation of the method.

This is a proof of concept.


- [Input](schema.json)
- [Output](method.md)


### Usage


```php
<?php

require 'src/generator.php';

$api_key   = 'YourAPIKey';
$generator = new DocGenerator($api_key);


$method_schema = 'schema.json'; // local file
#$method_schema = $argv[1]; // first CLI argument

$output = $generator->compile($method_schema);

file_put_contents('method.md', $output);

?>
```
