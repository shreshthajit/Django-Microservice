# Django-Microservice

# For SQL server I have used docker:
```
docker run --name mysql-db \
  --network django-network \
  -e MYSQL_ROOT_PASSWORD=rootpass \
  -e MYSQL_DATABASE=django_db \
  -e MYSQL_USER=shreshthajit \
  -e MYSQL_PASSWORD=password \
  -p 3306:3306 \
  -d mysql:8
  ```

# Migrate
```
python manage.py makemigrations
python manage.py migrate

```
# Command to create a network
```
docker network create django-network

```


Split terminal into 3 parts and Run the following command:

```
1. In EmailService folder: python manage.py launch_queue_listener
2. In UserService folder: python manage.py launch_queue_listener 
3. In UserService Folder: python manage.py runserver
```
