# Cinema Api

API service for cinema management written on DRF

### Installing using GitHub
Install PostgreSQL and create db


```
git clone https://github.com/kateryna3k/cinema-api
python3 -m venv venv
source venv/bin/activate (Linux and macOS) or venv\Scripts\activate (Windows)
pip install -r requirements.txt
set DB_HOST=<your db hostname>
set DB_NAME=<your db name>
set DB_USER=<your db username>
set DB_PASSWORD=<your db user password>
python manage.py migrate
python manage.py runserver
```


### Run with Docker

Docker should be installed

```
docker-compose build
docker-compose up
```

### Getting access

Create superuser:
   1. Get id of the docker container to access: `docker ps`
   2. Using this id, open the shell in the container: `docker exec -it <id> sh`
   3. Create superuser: `python manage.py createsuperuser`
   4. Provide the required credentials.

### Features
- JWT authenticated
- Admin panel /admin/
- Documentation is located at /api/doc/swagger/
- Managing orders and tickets
- Creating movies with genres, actors, images
- Creating cinema halls
- Adding movie sessions
- Filtering movies and movie sessions
