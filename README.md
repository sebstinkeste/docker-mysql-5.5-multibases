# docker-mysql-5.5-multibases

## Pré-requis

```
    Docker >= 1.9
    Docker-compose >= 1.5
```

##Installation

```
docker pull sebstinkeste/mysql:5.5-multibases
```

## Environment variables

### Set your my.cnf

The mysqld configuration is dynamic. Just add environment variable with prefix `MYSQLD__`.

Example with docker-compose :

    ...
    environment:
        MYSQL_DATABASE: 'database_name'
        MYSQL_DATABASE_2: 'database_name_2'
        MYSQLD__max_allowed_packet : '64M'
	...

Please see https://hub.docker.com/_/mysql/ for more details.
