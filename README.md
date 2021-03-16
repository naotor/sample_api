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
  └── uwsgi.d
      └── dev.ini

  $ vi .env
  ENV=dev
  API_NAME=sample_api

  $ docker-compose build

  $ docker-compose django-admin startproject sample_api

  $ docker-compose up -d
```
