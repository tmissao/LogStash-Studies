# LogStash - Studies

This project intends to summarize all the knowledge earned during my studies of logstash.

It can be divided into the following sections:


-  [`Introduction`](./01-Introduction.md)
-  [`Logstash Basics`](./02-LogstashBasics.md)
-  [`Manipulating Data`](./03-ManipulatingData.md) - Apache Web Server Project
-  [`Using Filebeat`](./04-Beats.md) - Apache Web Server using FileBeat and ELK stack

## Results
---
This is the final results of my studies:

1. Filebeat extracts data (access and error logs) from Apache Web Servers and send to Logstash.

2. Logstash manipulates the data, making transformations and data enrichments. After that, it sends to elasticsearch.

3. Elasticsearch stores the data and allows future queries and analyses.

4. Kibana retrieves data from Elasticsearch and presents it in a graphical form throught dashboards.

![Results](./artifacts/FinalProject.gif)

## References
---

- [Course - Logstash](https://www.udemy.com/share/101yeKCEQScl9X/)

- [Github](https://github.com/codingexplained/data-processing-with-logstash)