# PHP7 Standard dockerfile

This is a Docker image that inherits from drupaldocker/php:7.0-fpm-2.x
It contains standard overrides for NyMedia projects, everything that is reusable across projects.

To use, include it in your docker-compose.yml:

```
  php:
    image: nymediaas/php7-docker:latest
    networks:
      - back-tier
      - front-tier
    volumes:
      - ./:/var/www/html
    depends_on:
      - db
```
