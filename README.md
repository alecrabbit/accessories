# Abandoned!
project is moved to [alecrabbit/php-accessories](https://github.com/alecrabbit/php-accessories)

will be deleted soon

# PHP accessories

[![Minimum PHP Version](https://img.shields.io/badge/php-%3E%3D%207.2-8FA0BF.svg)](https://php.net/)
[![Build Status](https://travis-ci.org/alecrabbit/accessories.svg?branch=master)](https://travis-ci.org/alecrabbit/accessories)
[![Latest Stable Version](https://poser.pugx.org/alecrabbit/accessories/v/stable)](https://packagist.org/packages/alecrabbit/accessories)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/alecrabbit/accessories/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/alecrabbit/accessories/?branch=master)
[![Code Coverage](https://scrutinizer-ci.com/g/alecrabbit/accessories/badges/coverage.png?b=master)](https://scrutinizer-ci.com/g/alecrabbit/accessories/?branch=master)
[![Latest Stable Version](https://img.shields.io/packagist/v/alecrabbit/accessories.svg)](https://packagist.org/packages/alecrabbit/accessories)
[![Total Downloads](https://poser.pugx.org/alecrabbit/accessories/downloads)](https://packagist.org/packages/alecrabbit/accessories)
[![Latest Unstable Version](https://poser.pugx.org/alecrabbit/accessories/v/unstable)](https://packagist.org/packages/alecrabbit/accessories)
[![License](https://poser.pugx.org/alecrabbit/accessories/license)](https://packagist.org/packages/alecrabbit/accessories)

### Installation
```bash
composer require alecrabbit/accessories
```


### Usage
see [examples](https://github.com/alecrabbit/accessories/tree/master/examples)


### Features
- G - class containing generator functions
```php
$r1 = G::range(1, 3); 
$r2 = G::rewindableRange(1, 3); 
```
- Circular - helper class to get values in a circle
```php
$c = new Circular([1, 2, 3]);
$value = $c(); // invoke 
$value = $c->getElement(); // method 
```
- Rewindable - rewindable generator helper class
```php
$r = new Rewindable($generatorFunction);
iterator_to_array($r);
$r->rewind();
```
- Pretty - string formatter, e.g. bytes and time
```php
Pretty::bytes(10584760, 'mb'); // string(7) "10.09MB"
Pretty::time(0.214); // string(5) "214ms"
Pretty::precent(0.214); // // string(6) "21.40%"
```
- MemoryUsage - memory usage :)
```php
$report = MemoryUsage::report('mb');
echo $report . PHP_EOL;
```
