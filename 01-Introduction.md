# Introduction

Logstash is an open source event processing engine, in other words, logstash works as a data pipeline receiving, transforming and shipping data to a destination.

## Logstash Pipeline
---

It is an orchestration of plugins that: receives, manipulates or ships data.

A pipeline is composited by 3 phrases:

- `input` - Receives Events

- `filter` - Manipulates Events

- `output` - Ships the result to a destination (stashes)

## Installing
---

 - [`Install Java 8`](https://www.oracle.com/java/technologies/javase-downloads.html)

 - [`Install LogStash`](https://www.elastic.co/downloads/logstash)

 ```bash
tar -zxvf logstash-7.12.1-linux-x86_64.tar.gz
mv logstash-7.12.1 logstash
 ```

 These are the files:

 - config - Configures LogStash Execution, like pipelines, JVM etc
 
 - data - Contains data that logstash uses internally
 
 - logs - Where logstash files can be found.

 - bin - Binaries files and plugins to execute logstash

 ```bash
 # Testing LogStash

 cd logstash;
 bin/logstash -e "input { stdin { } } output { stdout { }  }"
 ```

 ## Running on Docker
 ---
```bash

# docker run --rm -it -v <volume-with-pipeline>:/usr/share/logstash/pipeline/ -p 8080:8080 docker.elastic.co/logstash/logstash:7.12.1

 docker run --rm -it \
  -v $(pwd)/pipelines/:/usr/share/logstash/pipeline/ \
  -p 8080:8080 \
  docker.elastic.co/logstash/logstash:7.12.1
```

## AutoReload Configuration
---

```bash
#bin/logstash -f <pipeline-config-path> --config.reload.automatic

bin/logstash -f config/pipelines/pipeline.conf --config.reload.automatic
```