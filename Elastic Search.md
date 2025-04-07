# [Github](https://github.com/codingexplained/complete-guide-to-elasticsearch)


![[Pasted image 20250403223001.png]]

![[Pasted image 20250403223609.png]]

## Scope of the Elastic Search:
- Elasticsearch - not the entire Elastic Stack

## What wil you learn:
- How to write complrex queriees:
	- Eg:
		- for search
		- data analysis
		- APM - Application Performance Management
		- server monitoring
		- security
- Examples of what is covered:
	- Mapping
	- analyzers
	- synonyms
	- stemming
	- search-as-you-type
	- auto-completion
	- highlighting
	- relevance tuning
	- aggregations

## Elasticsearch:
- open-source analytics & full-text search engine
- often used for search functionalities in applications (blog, ecommerce)
- build complex search queries
- queries structure data
- write queries to aggregate the data
- analyze application logs and system metrics
	- errors and CPU memory usage
	- APM
- Send events to Elasticsearch
	- eg:
		- sales
		- website clicks
		- phone calls
- Excellent at analysing lots of data
	- Forecast futures values with machine learning based on historical data
- Elastic search can be used for many different things
	- ***SEARCHING***
- **Data is stored as documents (JSON objects)**
	- similar to rows in relational database (eg: MySQL)
- **A document's data is separated into fields**
	- similar to columns in relational databsaeas
- ![[Pasted image 20250403230726.png]]
- 

## Querying Elasticsearch
- query documents is to use REST API
- ![[Pasted image 20250403231001.png]]
- Elasticsearch written in Java, built on top on Apache Lucene
- Easy to use and highly scalable
- scales very well in case of data volumes increase and query throughput

## Overview of the Elastic Stack
- Elastic Stack:
	- Technologies and tools developed/maintained by the company who created Elasticsearch BV
- Consists of:
	- X-PACK
	- KIBANA
	- BEATS
	- LOGSTASH
	- ELASTICSEARCH
- KIBANA:
	- AN analytics and visualisation platform
	- Use many built-in visualisation
	- Can manage parts of Elasticsearch and Logstash such as Authentication and Authorization
	- **Web interface for the data stores in the Elasticsearch**
	- Build dashboards with number of metrics!
- LOGSTASH:
	- Used to process logs from applications and send them to Elasticsearch
	- **It is horizontally scalable!**
	- Evolved to general purpose tool:
		- **It is a data processing pipeline**
	- Logstash PIPELINE s defined in a proprietery markup format that is similar to the JSON, where we can also add if condiitons to make it more dynamic.
	- ![[image.png]]
	- ![alt text](image.png)
	- Data that LOGSTASH receives will be handled as events which can be anything of your choice
		- Such as
			- Log file entires
			- e-commerce orders
			- customers
			- chat messages
		- These events are then processes by Logstash and shipped off to one or more destinations
			- Eg:
				- Elasticsearch
				- a kafka queue
				- email message
				- to an HTTP endpoint
	- LOGSTASH pipeline consists of 3 parts/stages:
		- Inputs
		- Filters
		- Outputs 
	- Each stage can make use of a so called **PLUGIN**
	- Inputs:
		- **Are how logstash receives events**
		- A input plugin could be a file for instance meaning that Logstash will read events from a given file
		- It could also be that we are sending events to Logstash over HTTP, or we could look up rows from a relational database, or listen to a Kafka queue.
	- Filters:
		- **Are all about how the Logstash should process them**
		- We can parse CSV, XML, JSON
		- Can do data enrichment
			- such as looking up an IP address and resolving its geographical location.
	- Outputs:
		- WHere we send the process events to.
		- **Formally, those places are called STASHES.**
		- LOGSTASH receives the events from ne or more inputs, process them and send thems to one or more stashes.
	- ![content_parsed-to-logstash](content_parsed-to-logstash.png)
- X-Pack:
	- 
	