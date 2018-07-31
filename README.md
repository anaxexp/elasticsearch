# Elasticsearch Docker Container Image

[![Build Status](https://travis-ci.org/anaxexp/elasticsearch.svg?branch=master)](https://travis-ci.org/anaxexp/elasticsearch)
[![Docker Pulls](https://img.shields.io/docker/pulls/anaxexperience/elasticsearch.svg)](https://hub.docker.com/r/anaxexperience/elasticsearch)
[![Docker Stars](https://img.shields.io/docker/stars/anaxexperience/elasticsearch.svg)](https://hub.docker.com/r/anaxexperience/elasticsearch)
[![Docker Layers](https://images.microbadger.com/badges/image/anaxexperience/elasticsearch.svg)](https://microbadger.com/images/anaxexperience/elasticsearch)

## Docker Images

!!! For better reliability we release images with stability tags (`anaxexperience/elasticsearch:6-X.X.X`) which correspond to [git tags](https://github.com/anaxexp/elasticsearch/releases). We **STRONGLY RECOMMEND** using images only with stability tags. 

Overview:

* All images are based on Alpine Linux
* Base image: [anaxexperience/openjdk](https://github.com/anaxexp/openjdk)
* [TravisCI builds](https://travis-ci.org/anaxexp/elasticsearch) 
* [Docker Hub](https://hub.docker.com/r/anaxexperience/elasticsearch)

Supported tags and respective `Dockerfile` links:

* `6`, `6.2`, `latest` [_(Dockerfile)_](https://github.com/anaxexp/elasticsearch/tree/master/Dockerfile)
* `6.1` [_(Dockerfile)_](https://github.com/anaxexp/elasticsearch/tree/master/Dockerfile)
* `6.0` [_(Dockerfile)_](https://github.com/anaxexp/elasticsearch/tree/master/Dockerfile)
* `5`, `5.6` [_(Dockerfile)_](https://github.com/anaxexp/elasticsearch/tree/master/Dockerfile)
* `5.5` [_(Dockerfile)_](https://github.com/anaxexp/elasticsearch/tree/master/Dockerfile)
* `5.4` [_(Dockerfile)_](https://github.com/anaxexp/elasticsearch/tree/master/Dockerfile)

## Environment Variables

| Variable                                      | Default Value           | Description |
| --------------------------------------------- | ----------------------- | ----------- |
| `ES_JAVA_OPTS`                                | `-Xms1g -Xmx1g`         |             |
| `ES_CLUSTER_NAME`                             | `elasticsearch-default` |             |
| `ES_NODE_MASTER`                              | `true`                  |             |
| `ES_NODE_DATA`                                | `true`                  |             |
| `ES_NODE_INGEST`                              | `true`                  |             |
| `ES_HTTP_ENABLED`                             | `true`                  |             |
| `ES_NETWORK_HOST`                             | `0.0.0.0`               |             |
| `ES_HTTP_CORS_ENABLED`                        | `true`                  |             |
| `ES_HTTP_CORS_ALLOW_ORIGIN`                   | `*`                     |             |
| `ES_DISCOVERY_ZEN_MINIMUM_MASTER_NODES`       | `1`                     |             |
| `ES_NODE_MAX_LOCAL_STORAGE_NODES`             | `1`                     |             |
| `ES_SHARD_ALLOCATION_AWARENESS_ATTR`          |                         |             |
| `ES_SHARD_ALLOCATION_AWARENESS_ATTR_FILEPATH` |                         |             |
| `ES_BOOTSTRAP_MEMORY_LOCK`                    | `true`                  |             |
| `ELASTIC_CONTAINER`                           | `true`                  |             |

## Orchestration Actions

Usage:
```
make COMMAND [params ...]
 
commands:
    check-ready [host max_try wait_seconds delay_seconds]
 
default params values:
    host localhost
    max_try 1
    wait_seconds 1
    delay_seconds 0
```

## Deployment

Deploy Elasticsearch with Kibana to your own server via [![AnaxExp](https://www.google.com/s2/favicons?domain=anaxexp.io) AnaxExp](https://anaxexp.io).
