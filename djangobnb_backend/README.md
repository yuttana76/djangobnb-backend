# Django Backend & Docker Compose

### Create virtual environment
```
python -m venv env
```

Activate virtual environment
>source env/bin/activate

Deactivate virtual environment
>deactivate

```
pip install django
```

Create Django project
>django-admin startproject djangobnb_backend .

### Create Docker file & Docker Compose file

```
docker compose build
docker compose up -d
docker compose up --build
```

Run django migrte in container
'''
docker compose exec web python manage.py migrate
'''

chmod +x ./djangobnb_backend/entrypoint.sh

### Creeate user account app.
```
docker-compose exec web python manage.py startapp useraccount
```