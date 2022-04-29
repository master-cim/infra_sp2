![](https://img.shields.io/badge/Python-3.7.5-blue) 
![](https://img.shields.io/badge/Django-2.2.16-green)
![](https://img.shields.io/badge/DjangoRestFramework-3.12.4-red)
![](https://img.shields.io/badge/Docker-3.8-yellow)
<br><br>
## Название проекта
**«YaMDb API»** - проект YaMDb собирает отзывы пользователей на различные произведения.

**Возможности приложения:**<br>
:black_small_square: Регистрация на сайте, получение токена, изменение данных своей учетной записи<br>
:black_small_square: Раздаление прав пользователей согласно, назначенной ему роли<br>
:black_small_square: Возможность, согласно авторизации выполнять следующие дествия: получать, добавлять и удалять - категорию, жанр, произведение, отзыв и комментарий<br>
:black_small_square: Администрирование пользователями<br><br>


## :computer: Технологии в проекте

:small_blue_diamond: Python <br>
:small_blue_diamond: Django <br>
:small_blue_diamond: Django REST Framework <br>
:small_blue_diamond: Docker <br>


## :pencil2: Инструкции по запуску
Для того чтобы развернуть образ на локальной машине, выполнитеследующиедействия.
1. Авторизоваться через консоль:
```sh
docker login -u <имя пользователя>
```
2. Загрузка образа с DockerHub
```sh
docker pull mastersup/infra:v1.04.2022
```
3. Проверьте, что образ в системе.
```sh
docker images
```
4. Запустите Докер-контейнер с этим образом:
```sh
docker-compose up -d
```
5. Проверьте в отдельном окне bush состояние контейнера:
```sh
docker ps
```
6. Скопируйте ID контейнера infra_web, используйте команду для доступа информации:
```sh
docker container ls
```
7. Зайдите внутрь контейнера через консоль Bash:
```
docker exec -it <ID_контейнера> bash
```
8. Выполинте последовательно миграции и создание суперпользователя:
```sh
python manage.py makemigrations
python manage.py migrate
python manage.py createsuperuser
```
9. Наполнить БД тестовыми данными выполнив команду:
```sh
python manage.py dbfill
```
10. Запустить проект:
```sh
python manage.py runserver
```
11. Проверьте доступность сервиса
```sh
http://localhost/admin
```
<br>
## :books: Переменные среды
Этот образ использует переменные среды для настройки. Добавьте файл .env в папку infra и заполните переменные необходимыми значениями.

|Переменные              |Значение Default               |Описание                                            |
|------------------------|-------------------------------|----------------------------------------------------|
|`DB_ENGINE`             |`django.db.backends.postgresql`|Указываем движок БД                                 |
|`DB_NAME`               |`postgres`                     |Имя базы данных                                     |
|`POSTGRES_USER`         |no default                     |Логин дляподключения к БД                           |
|`POSTGRES_PASSWORD`     |no default                     |Пароль для подключения к БД                         |
|`DB_HOST`               |`db`                           |Название сервиса (контейнера)                       |
|`DB_PORT`               |5432                           |Порт для подключения к БД                           |


<br>

## :bust_in_silhouette: Автор проекта 
### :small_orange_diamond: Светлана  Петрова _(Svetlana Yu. Petrova)_
```html
e-mail: master-cim@yandex.ru
```
```html
https://github.com/master-cim
```
![Svetlana Yu. Petrova](https://sun9-69.userapi.com/s/v1/ig2/xnnSHqXZgIfndCNtTIc6uvOkDxJpBby-YbjsRuwBUMRWD3i70InOYiPjQ2S-7AX74uYWWXo6CYDZbjkFCPGr7Wtl.jpg?size=319x319&quality=96&type=album "Svetlana Yu. Petrova")
