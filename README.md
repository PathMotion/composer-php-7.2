# composer-php-7.2 [![Build Status](https://travis-ci.org/PathMotion/composer-php-5.6.svg?branch=master)](https://travis-ci.org/PathMotion/composer-php-5.6)
Composer image with Php 7.2 and XDebug extension enabled for running CI with code coverage capabilities.

## Description
This image contains:
 - php 7.2.14
 - composer 1.8.0
 - XDebug 2.6.0

## Usage
### Build the image
```
docker build -t image_name .
```

### Run container
From any Php 5.6 project directory you want to install, run `composer install` from the container:
```
docker run -it --rm -v $PWD:/app image_name install
```

If you need more commands, run `bash` from the container:
```
docker run -it --rm --entrypoint /bin/bash -v $PWD:/app raf-php
```
Then, run any commands like `phpunit` for instance:
```
root@a1b2c3:/app# ./vendor/bin/phpunit
```
### Warning
This image is meant to be used for development or CI environments. This is not Production grade.
