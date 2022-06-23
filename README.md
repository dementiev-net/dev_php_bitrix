# Окружение Bitrix (Nginx, PHP, Mysql)

### Подключение к MySQL

* Хост БД: mysql5.7
* Пользователь: root
* Пароль: root
* phpMyAdmin: http://localhost:8081/

### Работа с разными версиями PHP

По умолчанию используется PHP 7.4.
Чтобы выбрать версию PHP нужно редактировать файл ``docker-compose.yml``.

### Отправка e-mail'ов

PHP по умолчанию не отправляют настоящих писем при вызове функции ``mail()``.
Все исходящие e-mail'ы перехватываются и пишутся в папку ``app/log/sendmail``.

### Поддержка xDebug для PHP

xDebug уже настроен для использования в контейнерах с PHP7 и PHP8. Для его включения нужно раскомментировать установку модуля в ``config/php*/Dockerfile``.
О настройке PHPStorm для работы с Docker и xDebug 3 можно прочитать в статье [PHP: Настраиваем отладку](https://handynotes.ru/2020/12/phpstorm-php-8-docker-xdebug-3.html).
