# API для YaTube

## Описание

API для YaTube - web-приложение реализующее социальную сеть, позволяющее пользователям вести дневники, подписываться друг на друга и оставлять комментарии.

### Возможности
* Регистрация, аутентификация (JWT) и управление учётной записью
* Создание записей (постов) пользователя с возможностью загрузки изображения
* Создания комментарием к постам пользователей
* Подписка на записи выбранных авторов
* Реализованы кеширование и паджинация

### Технологии
* Python 3.7
* Django 2.2.16
* Django Rest Framework 3.12.4
* SQLite

## Как запустить проект

Клонировать репозиторий и перейти в корневую директорию проекта:

```
git clone https://github.com/Platser/YaTube-API.git
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:
```
python3 -m venv venv
source venv/bin/activate (или .\venv\scripts\activate для Windows)
```
Обновить pip:
```
python3 -m pip install --upgrade pip
```
Установить зависимости из файла requirements.txt:
```
pip install -r requirements.txt
```
Перейти в директорию с manage.py:
```
cd yatube_api
```
Выполнить миграции:
```
python3 manage.py migrate
```
Запустить проект:
```
python3 manage.py runserver
```
### Решение проблем
На некоторых ПК при работе с GitBash для Windows команда runserver зависает после вывода "Watching for file changes with StatReloader". В этом случае необходимо определить следующую переменную окружения:
```
export PYTHONUNBUFFERED=1
```
Выполнение некоторых команд manage.py при работе с GitBash для Windows приводит к возникновению ошибки, например такой:
```
Superuser creation skipped due to not running in a TTY.
```
В этом случае команду следует выполнять, добавив winpty:
```
winpty python manage.py createsuperuser
```
### Важные эндпоинты
http://127.0.0.1:8000/admin - панель администратора

### Примеры API-запросов
Проект сопровождается документацией, которая будет доступна после запуска сервера по адресу: `http://127.0.0.1:8000/redoc/`


## Автор
Денис Малашевич
Проект разработан в рамках учебного курса **Яндекс.Практикум Python-разработчик**.

### Лицензия 
[Лицензия MIT](https://opensource.org/licenses/MIT)
