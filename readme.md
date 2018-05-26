# How to run #

cd build/container/dev
docker-compose up -d

# First run #

docker-compose exec php-fpm composer update
docker-compose exec php-fpm ./vendor/bin/simple-phpunit


# Running tests #

docker-compose exec php-fpm composer test

This will run the composer script: SYMFONY_PHPUNIT_REMOVE=\"symfony/yaml\" ./vendor/bin/simple-phpunit

SYMFONY_PHPUNIT_REMOVE is required to get prophecy working with Symfony.
