# Django Backend & Docker Compose
super user
    admin
    yuttaa@gmail.com
    password

    xxx@gmail.com
    xxx@password


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
docker exec web python manage.py migrate
'''

chmod +x ./djangobnb_backend/entrypoint.sh

### Creeate user account app.
```
docker exec backend-web-1 python manage.py startapp useraccount
docker exec backend-web-1 python manage.py startapp property
docker exec backend-web-1 python manage.py startapp chat

```

Update setting.py 

```
docker exec web python manage.py makemigrations
docker exec web python manage.py flush  # remove all in db

docker exec -it backend-web-1 python manage.py createsuperuser
```

### Implement property model
-model.py
-serializers.py
-api.py
-urls.py
-admin.py


### Creeate chat app.
```
docker exec backend-web-1 python manage.py startapp chat

```

### Install web sockets
channels==4.0.0
daphne==4.0.0
TIME: 9:46


### Search api

### Deployment Backend to DigitalOcean
12:16

ssh
>apt update

### Build & run docker in server
Clone project from git
>docker compose -f docker-compose.prod.yml up --build

### Deployment Frontend to DigitalOcean
