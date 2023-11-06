![Static Badge](https://img.shields.io/badge/Python-14354C?style=for-the-badge&logo=python&logoColor=white) ![Static Badge](https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white)
![Static Badge](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
# Dockerize Django and Postgres

## Description
-----------
This is a mini tutorial for containerising (Dockerize) Reactified Django.
The frontend and the backend both served by the same server. (port 8000, in case of developemnt)

## Steps to Run
1. Clone the repo
2. Install node dependencies (Needed only first time install):
`npm install --prefix app`
3. Build react: `npm run build --prefix app`
4. Build the docker images: `docker compose build`
5. Run the containers: `docker compose up -d`
6. (For 1st time) Create a superuser: `docker-compose exec django python manage.py createsuperuser`
7. Open Browser and goto: `http://localhost:8000`
8. Shut down docker containers: `docker compose down`


## Additional commands
#### Collect static

```bash
docker compose exec django python manage.py collectstatic
```

#### Create Migrations

```bash
docker compose exec djano python manage.py makemigrations
```

#### Migrate DB

```bash
docker compose exec django python manage.py migrate
```
