# taski-docker
### Описание проекта 
taski - сервис для любителей котиков.

Что умеет проект:

- Добавлять, просматривать, редактировать и удалять котиков.
- Добавлять новые и присваивать уже существующие достижения. 
- Просматривать чужих котов и их достижения.

### Технологии
- Python 
- Django 
- API DRF 
- Docker 
- GitHub

### Запуск проекта:
1. Клонируйте проект:
```commandline
git@github.com:gleb60/taski-docker.git
```
2. Скопируйте файлы с локального компьютера на сервер:
```
scp docker-compose.yml <username>@<host>:/home/<username>/
scp nginx.conf <username>@<host>:/home/<username>/
scp .env <username>@<host>:/home/<username>/
```
3. Установите docker и docker-compose:
```
sudo apt install docker.io 
sudo apt install docker-compose
```
4. Соберите контейнер, выполните миграции, создайте суперюзера и соберите статику:
```
sudo docker-compose up -d --build
sudo docker-compose migrate
sudo docker-compose exec backend python manage.py createsuperuser
```
