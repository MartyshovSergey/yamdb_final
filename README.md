# API_YAMDB
![yamdb_workflow](https://github.com/martyshovsergey/yamdb_final/workflows/yamdb_workflow/badge.svg)
Проект для публикаций отзывов пользователей на произведения. Категории произведений: «Книги», «Фильмы», «Музыка». Список категорий расширяемый.

Читатели оставляют к произведениям текстовые отзывы (Review) и выставляют рейтинг (оценку в диапазоне от 1 до 10).

## Запуск проекта

1. Клонировать репозиторий:
```
git clone git@github.com:MartyshovSergey/infra_sp2.git
```

2. В корневой директории создать файл .env:
```
DB_ENGINE=django.db.backends.postgresql
DB_NAME=postgres
POSTGRES_USER=postgres
POSTGRES_PASSWORD=postgres
DB_HOST=db
DB_PORT=5432
```

3. Запустить docker-compose
```
docker-compose up
```

4. В WEB контейнере выполнить миграции:
```
docker-compose exec web python manage.py migrate
```

5. Создать суперпользователя:
```
docker-compose exec web python manage.py createsuperuser
```

6. Собрать статику:
```
docker-compose exec web python manage.py collectstatic --no-input
```
