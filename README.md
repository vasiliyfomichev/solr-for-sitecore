What is Solr for Sitecore?
================
Solr is highly reliable, scalable and fault tolerant, providing distributed indexing, replication and load-balanced querying, automated failover and recovery, centralized configuration and more. Solr for Sitecore offeres a preconfigured solution for Sitecore CMS, which already has all required cores and is ready out of the box with default configuration to be connected to a Sitecore instance.

Learn more on [Apache Solr homepage](http://lucene.apache.org/solr/) and in the [Apache Solr Reference Guide](https://www.apache.org/dyn/closer.cgi/lucene/solr/ref-guide/).

Learn more about Sitecore on [Sitecore website](http://www.sitecore.net/), [Sitecore Documentation Portal](https://doc.sitecore.net/) and [Sitecore Community Portal](https://community.sitecore.net/).


To learn how to create and configure your own image of Solr for Sitecore refer to Sitecore Best Practices Articles: 

- How to Setup Mongo and Solr on Docker for Sitecore xDB: Part 1
- How to Setup Mongo and Solr on Docker for Sitecore xDB: Part 2



> [wikipedia.org/wiki/Apache_Solr](http://wikipedia.org/wiki/Apache_Solr)


![Solr for Sitecore](http://www.cmsbestpractices.com/wp-content/uploads/2015/07/solr-for-sitecore-logo.png)

How to run a Solr for Sitecore instance:
--------------------------------------------------


``` 
docker run -d -p 8983:8983 -t vasiliyfomichev/solr-for-sitecore:{tag}
```

Then with a web browser go to _http://{host IP}:8983/solr_ to see the Admin Console (adjust the hostname for your docker host).


Supported Docker versions
---------------------------------------
This image has been tested with Docker version 1.7.0.

License
------------
Solr is licensed under the Apache License, Version 2.0, and this repository is too:

Copyright 2015 Vasiliy Fomichev

Licensed under the Apache License, Version 2.0 (the “License”); you may not use this file except in compliance with the License. You may obtain a copy of the License at

[http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)


Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an “AS IS” BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the Licens