# Laradock (slim)

This is a slimmed down version of Laradock intended as a base for some of **my** production use cases. You'll probably want to visit [the main repo](https://github.com/laradock/laradock) and / or fork your own instead.

## Containers:
* workspace (slimmed down)
* php-fpm
* php-worker
* laravel-horizon
* nginx
* mysql
* redis
* mailhog

## Usage:
* `git submodule add https://github.com/shaneparsons/laradock`
* `cp env-example .env`
  * change mysql credentials in .env
* `cd laradock && docker-compose up -d`

