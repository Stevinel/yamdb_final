# api_yamdb
![yatube_final](https://github.com/github/docs/actions/workflows/main.yml/badge.svg)

## Описание
API для проекта yamdb.

### Технологии
- Python
- Django
- DRF
- PostgreSQL
- nginx
- Docker

### Требования
Необходим установленный и запущенный Docker.

Инструкции по установке см. [Docker](https://www.docker.com/get-started#h_installation)

### Первый запуск проекта
     
1. Клонирование репозитория 
```
git clone https://github.com/Stevinel/infra_sp2
```
2. Сборка и запуск образа 
```
- docker-compose up -d --build
```
3. Создание миграций
```
- docker-compose exec web python manage.py makemigrations
```
4. Применение миграций
```
- docker-compose exec web python manage.py migrate
```
5. Сбор статики
```
- docker-compose exec web python manage.py collectstatic
```
6. Создание учетной записи администратора
```
- docker-compose exec web python manage.py createsuperuser
```
7. Загрузка в базу тестовых данных (по желанию) 
```
- docker-compose exec web python manage.py loaddata fixtures.json
```

### Регулярный запуск       
```bash
- docker-compose up
```
