# php8.1-dev

* docker-compose.yml example

```yaml
    php:
        user: 1000:www-data
        image: dvlpm/php8.1-dev:latest
        volumes:
            - ./:/var/www/html
            - ./volumes/php/usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini:/usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini
        environment:
            XDEBUG_CONFIG: remote_host=192.168.99.1
```

docker-php-ext-xdebug.ini containts

```
display_errors = 1

zend_extension=xdebug.so
xdebug.remote_enable=on
xdebug.remote_autostart=on
```
