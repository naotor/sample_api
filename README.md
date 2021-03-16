# sample_api
Sample API Environment

```
  $ tree .
  .
  ├── Dockerfile
  ├── LICENSE
  ├── README.md
  ├── conf.d
  │   └── nginx
  │       ├── nginx.conf
  │       └── uwsgi_params
  ├── docker-compose.yml
  ├── env.d
  │   └── dev.env
  ├── requirements.txt
  ├── sql.d
  │   └── init.sql
  ├── src
  └── uwsgi.d
      └── dev.ini

  $ vi .env
  ENV=dev
  API_NAME=sample_api

  $ source .env

  $ docker-compose build

  $ docker-compose django-admin startproject $API_NAME

  $ sudo chown $USER:$USER -R src
  $ mv src/$API_NAME/manage.py src/
  $ mv src/$API_NAME/$API_NAME/* src/
  $ rmdir src/$API_NAME/$API_NAME

  $ docker-compose up -d
```
