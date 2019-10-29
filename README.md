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
```bash
git submodule add https://github.com/shaneparsons/laradock

cd laradock

cp env-example .env

# change mysql credentials in .env

# if using laravel-horizon:

  cp laravel-horizon/supervisord.d/laravel-horizon.conf.example\
  laravel-horizon/supervisord.d/laravel-horizon.conf

# if using scheduling:

  cp php-worker/supervisord.d/laravel-scheduler.conf.example\
  php-worker/supervisord.d/laravel-scheduler.conf

  # Note: you can also add `laravel-horizon.conf` here, if both are needed.
  # this avoids needing to add `laravel-horizon` seperately

docker-compose up -d
```
