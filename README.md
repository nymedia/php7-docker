# PHP7 Standard dockerfile

This is a Docker image that inherits from drupaldocker/php:7.x-fpm-2.x and drupaldocker/php:7.x-cli-2.x.

It contains standard overrides for Ny Media projects, everything that is reusable across projects.

To use, include it in your docker-compose.yml (specify the version you want in the tag, the part after the colon, in the example 7.1):

```
  php:
    image:  nymediaas/php7-docker:7.1-cli
    networks:
      - back-tier
      - front-tier
    volumes:
      - ./:/var/www/html
    depends_on:
      - db
```
