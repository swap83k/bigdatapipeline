# Spark setup using Docker

## Commands

Building docker image
```
docker build -t cluster-apache-spark:3.0.2 .
```

Running docker compose
```
docker-compose up -d
```

Connecting to master node
```
docker ps
winpty docker-compose exec spark-master bash
```

Connecting to postgres db
```
docker exec -it 7d03278b70f1 bash // container id of postgresql
winpty docker exec -it 7d03278b70f1 psql -U postgres
psql -U postgres
create database mta_data
```

Reference repo for setup: https://github.com/mvillarrealb/docker-spark-cluster