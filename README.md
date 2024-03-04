# EFK-Stack-Docker

# Elasticsearch-Filebeat-Kibana stack to monitor Nginx logs

## Contents
- Nginx: containing build image nginx web server
- Elasticsearch: containing build image and configuration for Elasticsearch
- Filebeat: containing build image and configuration for Filebeat to stream nginx logs Elasticsearch
- Kibana: containing build image and configure for Kibana to visualize data from an Elasticsearch index

## How it works

- Nginx access and error logs are written to a directory. The directory is mapped to a local volume.
- Filebeat reads the nginx logs from the local volume and sends it to an Elasticsearch index [filebeat-*].
- Kibana uses the index to visualize the access and the error logs.

## How to run it

Pre-requisitesbash
- docker
- docker-compose
To run this stack, run the following command
bash
docker-compose up -d
Accessing the components :

nginx  : http://localhost

Kibana : http://localhost:5601

Kibana credentials :
- Username: elastic
- Password: changeme%

# Elasticsearch-Filebeat-Kibana Docker Stack for Nginx Logs Monitoring

This Docker Compose project sets up an Elasticsearch-Filebeat-Kibana stack to monitor Nginx access and error logs.

## Contents
- **Nginx:** Docker image for the Nginx web server.
- **Elasticsearch:** Docker image and configuration for Elasticsearch.
- **Filebeat:** Docker image and configuration for Filebeat to stream Nginx logs to Elasticsearch.
- **Kibana:** Docker image and configuration for Kibana to visualize data from the Elasticsearch index.

## How it works

1. Nginx access and error logs are written to a directory, mapped to a local volume.
2. Filebeat reads the Nginx logs from the local volume and sends them to an Elasticsearch index [filebeat-*].
3. Kibana uses the index to visualize the access and error logs.

## How to run

### Prerequisites
- Docker
- Docker Compose

### Run the stack
```bash
docker-compose up -d

```



# A sample visualisation from the kibana dashboard showing number of requests for nginx file in a given time:


![Screenshot from 2024-02-28 23-13-39](https://github.com/SharanReddyy/EFK-Stack-Docker-/assets/78129496/83e1fd16-db11-4165-9b5a-6d54fe1f9040)


