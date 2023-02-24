## Описание

Проект YaMDb собирает отзывы пользователей на произведения.
Произведения делятся на категории: «Книги», «Фильмы», «Музыка».
### Как запустить проект:

```bash
docker-compose up

docker-compose exec web python manage.py makemigrations reviews

docker-compose exec web python manage.py migrate

docker-compose exec web python manage.py createsuperuser

docker-compose exec web python manage.py collectstatic --no-input
```

Создание дампа БД:
```bash
docker-compose exec web python manage.py dumpdata > fixtures.json
```

### Шаблон наполнения .env (расположен по пути infra/.env)
```
DB_ENGINE=django.db.backends.postgresql
DB_NAME=postgres
POSTGRES_USER=postgres
POSTGRES_PASSWORD=postgres
DB_HOST=db
DB_PORT=5432
```
