# yamdb_final
yamdb_final

![Main workflow](https://github.com/Hangman91/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)

Проект на боевом находится по адресу:
http://51.250.100.192/

Админка: 
http://51.250.100.192/admin/

# api_yamdb
### Описание проекта:

Данный проект реализует REST api для системы управления отзывами на произведения,
с возможностью комментирования данных отзывов

### Технологии:

Python3, Django, Django REST framework, Nginx, Docker

### Документация

Всю документацию, примеры эндпоинтов и инструкцию по составлению запросов можно найти локально по ссылке:

```
127.0.0.1:8000/redoc/
```


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

## Как развернуть проект через докер:

1. Готовим сервер:
Останавливаем службу nginx:
sudo systemctl stop nginx 

2. Устанавливаем docker:
sudo apt install docker.io 

3. Устанавливаем docker-compose:
https://docs.docker.com/compose/install/

4. Копируем файлы docker-compose.yaml и nginx/default.conf на сервер в home/<ваш_username>/docker-compose.yaml и home/<ваш_username>/nginx/default.conf соответственно.

5. Клонируем проект:
git@github.com:Hangman91/yamdb_final.git

6. Разворачиваем проект: 
docker-compose up -d

7. Накатываем миграции
docker-compose exec web python manage.py migrate

7. Создаём суперюзера
docker-compose exec web python manage.py createsuperuser

8. Собираем статику
docker-compose exec web python manage.py collectstatic --no-input 

9. Импортируем базу данных
docker-compose exec web python manage.py loaddata дамп_бд.json


## Немного об авторе:
Александр, 30 лет, Санкт-Петербург.

Защитил  кандидатскую, работаю в Горном университете. 
Занимаюсь приёмом абитуриентов, профориентацией, проведением олимпиад. 
По совместительству преподаватель кафедры Метрологии.

Привет, ревьюер =)