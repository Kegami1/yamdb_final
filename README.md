![example workflow](https://github.com/kegami1/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)

# Проект YaMDb


### Описание

Проект YaMDb собирает отзывы  пользователей на произведения.
Сами произведения в YaMDb не хранятся, здесь нельзя посмотреть фильм или послушать музыку.
Благодарные или возмущённые пользователи оставляют к произведениям текстовые отзывы и ставят произведению оценку в диапазоне от одного до десяти; из пользовательских оценок формируется рейтинг произведения.

API для "YaMDb" дает возможность взаимодействоть с функциональной частью "YaMDb" через API-сервис.

### Шаблон .env

```
DB_ENGINE=django.db.backends.postgresql 
DB_NAME=postgres 
POSTGRES_USER=postgres 
POSTGRES_PASSWORD=postgres 
DB_HOST=db 
DB_PORT=5432 
```

### Запуск
Клонируйте проект
```
git@github.com:Kegami1/yamdb_final.git
```

Соберите образ из корневой дирректории
```
docker build -t yamdb_final ./api_yamdb/
```

Перейдите в папку с файлом docker-compose и запустите проект
```
cd infra
```
```
docker-compose up -d --build
```

Выполните миграции
```
docker-compose exec web python manage.py migrate
```


### Автор

Ватагин Алексей summer-vatagin@yandex.ru
