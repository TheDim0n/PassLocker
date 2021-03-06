# PassLocker

Another secret keys storage tool.
> Please **use this project locally** for more security.

**Contents:**
1. [Technology stack](#stack)
2. [Download the project](#download)
3. [Setup environment variables](#envs)
4. [Run with Docker](#run)
---------
## Technology stack <a name="stack"></a>
[![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi)](https://fastapi.tiangolo.com/)[![Angular](https://img.shields.io/badge/angular-%23DD0031.svg?style=for-the-badge&logo=angular&logoColor=white)](https://angular.io/)[![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)](https://www.postgresql.org/)[![Nginx](https://img.shields.io/badge/nginx-%23009639.svg?style=for-the-badge&logo=nginx&logoColor=white)](https://nginx.org/)[![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)

## Download <a name="download"></a>
```
git clone https://github.com/TheDim0n/PassLocker.git passlocker
cd passlocker
git submodule update --init
```

## Environments <a name="envs"></a>
Create `.env` file in project directory:
```
SECRET_KEY= # secret key for generating JWT
DEFAULT_USER_LOGIN= # your username, must be at least 4 characters
DEFAULT_USER_PASSWORD= # your password, must be at least 8 characters
ACCESS_TOKEN_EXPIRES_MINUTES= # JWT lifetime in minutes
PROXY_PORT= # published port (of your machine)
```
## Run with Docker <a name="run"></a>
```
docker-compose up -d
```
or
```
docker-compose up --build -d
```
Navigate to `http://localhost:<PROXY_PORT>`
> Docs available at `http://localhost:<PROXY_PORT>/api/docs` or `http://localhost:<PROXY_PORT>/api/redoc`
