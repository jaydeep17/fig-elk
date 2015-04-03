# Docker ELK stack

Run the ELK (Elasticseach, Logstash, Kibana) stack with Docker and Docker-compose.

Based on 3 Docker images:

* [elasticsearch](https://github.com/docker-library/elasticsearch)
* [elk-logstash](https://github.com/jaydeep17/docker-elk-logstash)
* [elk-kibana](https://github.com/deviantony/docker-elk-kibana)

## Installation and use
1. Install [Docker](http://docker.io).
2. Install [Docker-compose](http://docs.docker.com/compose/install/).
3. Clone this repository
4. docker-compose up
5. nc localhost 5000 < /some/log/file.log
6. http://localhost:5601 to use Kibana 4.

This will create 3 Docker containers with Elasticsearch, Logstash and Kibana 4 running in them and connected to each other. Three ports are exposed for access:
* 5000: Logstash TCP input.
* 9200: Elasticsearch HTTP (With Marvel plugin accessible via [http://localhost:9200/_plugin/marvel](http://localhost:9200/_plugin/marvel))
* 5601: Kibana 4 web interface.


## Logging with bunyan

* Refer to [this article](http://www.thedreaming.org/2014/11/21/docker-logstash/#logging-with-bunyan)
