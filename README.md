What is Solr for Sitecore?
================
Solr is highly reliable, scalable and fault tolerant, providing distributed indexing, replication and load-balanced querying, automated failover and recovery, centralized configuration and more. Solr for Sitecore offeres a preconfigured solution for Sitecore CMS, which already has all required cores and is ready out of the box with default configuration to be connected to a Sitecore instance.

Learn more on [Apache Solr homepage](http://lucene.apache.org/solr/) and in the [Apache Solr Reference Guide](https://www.apache.org/dyn/closer.cgi/lucene/solr/ref-guide/).

Learn more about Sitecore on [Sitecore website](http://www.sitecore.net/), [Sitecore Documentation Portal](https://doc.sitecore.net/) and [Sitecore Community Portal](https://community.sitecore.net/).


To learn how to create and configure your own image of Solr for Sitecore refer to Sitecore Best Practices Articles: 

- [How to Setup Mongo and Solr on Docker for Sitecore xDB: Part 1](http://www.cmsbestpractices.com/how-to-setup-mongo-and-solr-on-docker-for-sitecore-xdb-part-one/)
- [How to Setup Mongo and Solr on Docker for Sitecore xDB: Part 2](http://www.cmsbestpractices.com/how-to-setup-mongo-and-solr-on-docker-for-sitecore-xdb-part-two/)



> [wikipedia.org/wiki/Apache_Solr](http://wikipedia.org/wiki/Apache_Solr)


![Solr for Sitecore](http://www.cmsbestpractices.com/wp-content/uploads/2015/07/solr-for-sitecore-logo.png)

How to run a Solr for Sitecore instance:
--------------------------------------------------

1. [Install Docker for Windows (boot2docker)](http://docs.docker.com/windows/step_one/)
2. Run the following command -

``` 
docker run -d -p 8983:8983 -t vasiliyfomichev/solr-for-sitecore:{tag}
```

Then with a web browser go to _http://{host IP}:8983/solr_ to see the Admin Console (adjust the hostname for your docker host).

If no tag is specified in the command above, the 150427_5.2.1 will be used, which will setup Solr with cores and schema based on Sitecore 8 rev. 150427 (Update 3).

Solr for Sitecore Tags
-----------------------------
Solr for Sitecore tags consist of two parts - {Sitecore revision}_{Solr version}. Make sure to use the right tag for the version of Sitecore you are running. Although all tags indicate a Sitecore revision, some can be used for Sitecore installs within that version.

Supported Docker versions
---------------------------------------
This image has been tested with Docker version 1.7.0.

Contributing
----------------------
If you have have a contribution for this repository, please send a pull request in [Github](https://github.com/vasiliyfomichev/solr-for-sitecore/pulls).

If you want to contribute to Solr, see the [Solr Resources](http://lucene.apache.org/solr/resources.html).

License
------------
Solr is licensed under the Apache License, Version 2.0, and this repository is too:

Copyright 2015 Vasiliy Fomichev

Licensed under the Apache License, Version 2.0 (the “License”); you may not use this file except in compliance with the License. You may obtain a copy of the License at

[http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)


Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an “AS IS” BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the Licens

Related Sitecore Projects
--------------------------------

- [Sitecore ADFS Authenticator Module](https://github.com/vasiliyfomichev/Sitecore-ADFS-Authenticator-Module) - Sitecore module for authenticating users using ADFS.
- [Sitecore SignalR Tools](https://github.com/vasiliyfomichev/signalr-sitecore-tools) - commonly used Sitecore tools rebuilt using SignalR technology providing live updates and a modern interface.
- [Sitecore Solr Term Highlighter](https://github.com/vasiliyfomichev/Sitecore-Solr-Search-Term-Highlight) - enables search term highlighting in Sitecore search results when used with Solr.
