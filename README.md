# yamdb_final
yamdb_final

![Main workflow](https://github.com/Hangman91/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)


# api_yamdb
### Описание проекта:

Данный проект реализует REST api для системы управления отзывами на произведения,
с возможностью комментирования данных отзывов

### Технологии:

Python3, Django, Django REST framework, Nginx, Docker

### Документация

Всю документацию можно найти локально по ссылке:

```
127.0.0.1:8000/redoc/
```

При запуске на боевом сами понимаете, что делать, какой ендпоинт прописывать.


## Как запустить проект локально:

Cоздать и активировать виртуальное окружение:

```
python -m venv venv
```

```
source venv/Scripts/activate
```

```
python -m pip install --upgrade pip
```

Установить зависимости из файла requirements.txt:

```
pip install -r ./api_yamdb/requirements.txt
```

Выполнить миграции:

```
python manage.py migrate
```

Запустить проект:

```
python manage.py runserver
```
