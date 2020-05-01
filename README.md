# Clipboard for PHP
Provide copying and pasting to the Clipboard for PHP.

PHP port of [atotto/clipboard](https://github.com/atotto/clipboard) except for the Windows part

> #### Requires PHP 7.2.0 and above

## Platforms:

* **OSX**
* **Linux, Unix/BSD**: Requires `xclip` or `xsel` to be installed
* * **Wayland**: Requires [wl-clipboard](https://github.com/bugaevc/wl-clipboard)
* **Android using Termux**: Requires Termux:API add-on 
* **Windows**: Copying works normally but pasting requires [paste.exe](https://www.c3scripts.com/tutorials/msdos/paste.html#exe) to be in PATH or it'll fallback to using powershell which a bit slow.

## Usage

```bash
composer require asvvvad/clipboard:dev-master
```

```php
require 'vendor/autoload.php';

$c = new Clipboard();

if ($c->isUnsupported() === false) {
	$c->writeAll('copied');
	echo $c->readAll(); // "copied"
}

```
## Used in:
My own [cply-php](https://github.com/asvvvad/cply-php)
