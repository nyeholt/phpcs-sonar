# PHPCS Generic Issue Import Format reporter 

AKA Sonarqube formatter for PHPCS reports output 

This has been taken from code contributed by Marek freezy Víger (https://github.com/freezy-sk) 
on the PHP_CodeSniffer repository that was never merged in 
(https://github.com/squizlabs/PHP_CodeSniffer/pull/2451). Have extracted for use in projects 
by adding this repository to your project, then running

## Installation

Due to some composer installer constraints, you'll need to add the security audit 
module to your root level composer json so that aliasing works as expected;

```
composer require --dev dealerdirect/phpcodesniffer-composer-installer:"0.7.1 as 0.6.0" pheromone/phpcs-security-audit:dev-master
composer require pheromone/phpcs-security-audit:dev-master
```

## Usage 

`./vendor/bin/phpcs --standard=Security --report=./vendor/symbiote/phpcs-sonar/src/Sonar.php path/ > report-file.json`