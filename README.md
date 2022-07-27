# Социальная сеть YaTube

### Описание

Учебный проект, завершающий тему Web-API учебного курса **Яндекс-Практикум Python-разработчик**.

### Как запустить проект

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/Platser/api_final_yatube.git
```

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение (Windows):

```
python -m venv env
```

```
. env/Scripts/activate
```

```
python -m pip install --upgrade pip
```

Установить зависимости из файла requirements.txt:

```
pip install -r requirements.txt
```

Выполнить миграции (Windows):

```
python manage.py migrate
```

Запустить проект:

```
python3 manage.py runserver
```

На некоторых ПК с Windows команда runserver зависает после вывода
 "Watching for file changes with StatReloader". В этом случае необходимо
 определить следующую переменную окружения:
```
export PYTHONUNBUFFERED=1
```
### Примеры API-запросов

Проект сопровождается документацией, которая будет доступна после запуска сервера по адресу: `http://127.0.0.1:8000/redoc/`
