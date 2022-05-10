Docker Compose for Elasticsearch
=======================

## Description

This is an example compose file for running Elasticsearch with Docker Compose.

### Kernel settings for elasticsearch

Elasticsearch needs to set vm.max_map_count to at least 262144. See [Install Elasticsearch with Docker](https://www.elastic.co/guide/en/elasticsearch/reference/current/docker.html#docker-prod-prerequisites).

## Usage

### Run Elasticsearch

Elasticsearch for single node (localhost:9200):

```
$ docker compose -f compose.yaml up -d
```

Elasticsearch and Kibana (localhost:5601):

```
$ docker compose -f compose.yaml -f compose-kibana.yaml up -d
```

Elasticsearch cluster:

```
$ docker compose -f compose-cluster.yaml up -d
```

Elasticsearch cluster and Kibana:

```
$ docker compose -f compose-cluster.yaml -f compose-kibana.yaml up -d
```

### Stop Fess

```
$ docker compose -f compose.yaml -f ...(snip)... down

```

### Remove Local Volumes

```
$ docker volume prune

```
