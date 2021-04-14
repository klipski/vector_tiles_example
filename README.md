# drawer-backend

## Description
This is a repository that contains example configuration for serving maps with vector tiles.

## Setup and installation
Create `.env` file from template file `env.template`.

```
# create postgres volume
docker volume create --name=postgis_db

# install and run database
docker-compose up -d postgis
```
Load initial data from `lubelskie.sql`

```
psql -h localhost -d db_name -U user < lubelskie.sql
```

```
# run all containers
docker-compose up -d
```

## Features
* PostgreSQL 13.1 with PostGIS
* Tegola
* Redis as vector tile cache
* Maputnik
