# DOCKER LARAVEL

## tahap awal
buat folder "mysql" untuk volume database

## install composer
```
docker-compose exec php php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"

docker-compose exec php php -r "if (hash_file('sha384', 'composer-setup.php') === '55ce33d7678c5a611085589f1f3ddf8b3c52d662cd01d4ba75c0ee0459970c2200a51f492d557530c71c15d8dba01eae') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"

docker-compose exec php php composer-setup.php

docker-compose exec php php -r "unlink('composer-setup.php');"
```

```
docker-compose exec mv composer.phar /usr/local/bin/composer
```

## install laravel

```
docker-compose exec php composer create-project laravel/laravel .

docker-compose exec php composer install

docker-compose exec php php /var/www/html/artisan migrate
```

