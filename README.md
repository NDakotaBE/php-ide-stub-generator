# PHP Ide Stub File Generator

Simple stub file generator for development environments.

Base idea: https://gist.github.com/ralphschindler/4757829

## Examples

See the "examples" directory!!!

### Ignoring certain methods / properties in Classes
You can now add the possibility to ignore a certain method, by providing the generator with 
the appropriate data.

If the ignoreTag passed allong is in the DocBlock, the generator will ignore the function and 
skip it in generation.

```php
$generator = new Z\IdeStubGenerator\Strategy\PSR0();
```
OR
```php
$generator = new Z\IdeStubGenerator\Strategy\OneFile();
```

If you call the `$generator->setTagToIgnore();` function it'll ignore the given tag e.g.:
```php
$generator->setTagToIgnore('@ignore');
```

### Z\IdeStubGenerator\Strategy\PSR0

```php
$generator = new Z\IdeStubGenerator\Strategy\PSR0();
$generator->setBaseDir(...); // required
// $generator->setFunctionsStubFileName('functions.stub.php'); // optional. Default: 'functions.php'
// $generator->setConstantsStubFileName('constants.stub.php'); // optional. Default: 'constants.php'

// $generator->setClasses(array('class_name', ...)); // optional
// $generator->setFunctions(array('function_name', ...)); // optional
// $generator->setConstants(array('constant_name'=>constant_value, ...)); // optional
$generator->generate();
```

### Z\IdeStubGenerator\Strategy\OneFile
```php
$generator = new Z\IdeStubGenerator\Strategy\OneFile();
$generator->setFilePath(...); // required

// $generator->setClasses(array('class_name', ...)); // optional
// $generator->setFunctions(array('function_name', ...)); // optional
// $generator->setConstants(array('constant_name'=>constant_value, ...)); // optional
$generator->generate();
```

## License

ISC License (ISC)

Copyright (c) 2014, Rácz Tibor Zoltán <racztiborzoltan+github@gmail.com>

Permission to use, copy, modify, and/or distribute this software for any purpose with or without fee is hereby granted, provided that the above copyright notice and this permission notice appear in all copies.

THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF OR IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.

#### Personal notes
  - Sorry for my bad english in the source code! :)
