Docker Compose for Elasticsearch
=======================

## Description

This is an example compose file for running Elasticsearch with Docker Compose.

## Usage

### Run Elasticsearch

Elasticsearch for single node:

```
$ docker-compose -f docker-compose.yml up -d
```

Elasticsearch and Kibana:

```
$ docker-compose -f docker-compose.yml -f docker-compose.kibana.yml up -d
```

Elasticsearch cluster:

```
$ docker-compose -f docker-compose.yml -f docker-compose.cluster.yml up -d
```

Elasticsearch cluster and Kibana:

```
$ docker-compose -f docker-compose.yml -f docker-compose.cluster.yml -f docker-compose.kibana.yml up -d
```

### Stop Fess

```
$ docker-compose -f docker-compose.yml -f ...(snip)... down

```

### Remove Local Volumes

```
$ docker volume rm compose_esdata01 compose_esdata02

```
