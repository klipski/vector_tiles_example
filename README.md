# vector_tiles_example

## Description
This repository contains example configuration for serving maps with vector tiles.

## Setup and installation
1. Create `.env` file from template file `env.template`.

2. Create postgres volume
    ```
   docker volume create --name=postgis_db
   ```
3. Install and run database
   ```
   docker-compose up -d postgis
   ```
4. Download example data from: http://51.75.67.50:8000/lubelskie.sql, and load it to your database by:
   ```
   psql -h localhost -d db_name -U user < lubelskie.sql
   ```
6. Run all containers
   ```
   docker-compose up -d
   ```

## Features
* Tegola at http://localhost:80
* Maputnik at http://localhost:8888
* PostgreSQL 13.1 with PostGIS
* Redis as vector tile cache
