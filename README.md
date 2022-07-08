# Окружение Bitrix (Nginx, PHP, Mysql)

### Docker

```console
// загрузка из HUB
docker images
docker login

docker pull dementievnet/phpmyadmin:v5.2.0
docker pull dementievnet/mysql:v8.0
docker pull dementievnet/nginx:v1.23.0
docker pull dementievnet/php:v7.4

// управление
docker-compose uo
docker-compose down

// пересборка
docker-compose up --build -d

// удаление неиспользованных контейнеров
docker system prune

// mysql
docker exec -it mysql /bin/bash
```

### Подключение к MySQL 8.0.29

* Хост БД: db
* Пользователь: root
* Пароль: 1234
* phpMyAdmin: http://localhost:8081/

### Nginx 1.23.0

...

### PHP 7.4.30

...

### Отправка e-mail'ов

PHP по умолчанию не отправляют настоящих писем при вызове функции ``mail()``.
Все исходящие e-mail'ы перехватываются и пишутся в папку ``app/log/sendmail``.

### Поддержка xDebug для PHP

xDebug уже настроен для использования в контейнерах с PHP7 и PHP8. Для его включения нужно раскомментировать установку модуля в ``config/php*/Dockerfile``.
О настройке PHPStorm для работы с Docker и xDebug 3 можно прочитать в статье [PHP: Настраиваем отладку](https://handynotes.ru/2020/12/phpstorm-php-8-docker-xdebug-3.html).
