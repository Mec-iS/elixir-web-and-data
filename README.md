# A notepad on Big-data Elixir and HTTP

## Common points for a distributed architecture

* Open source tools
* [Elixir](http://elixir-lang.org) can be the future of data handling and distribution on the Web
* Lambda or pseudo-lambda ? or whatever
* A close interaction among *Elixir* and *Python* tools and libraries (via Web interface or not)
* Low barriers in terms of learning curve and computation costs. 
* Data-scientists friendly: easy for smaller sets, growing complexity for analytic tools (map-reduce). 
* High scalability guaranteed by Erlang: from small focused datasets (data and aggregates) to cloud deployments, using microservices clusters and [Kubernetes](http://kubernetes.io)

## Links

### Hadoop

* [HttpFS (REST API for HDFS)](http://hadoop.apache.org/docs/current/hadoop-hdfs-httpfs/index.html)
* [C API libhdfs](http://hadoop.apache.org/docs/current/hadoop-project-dist/hadoop-hdfs/LibHdfs.html) - could be wrapped with an Elixir NIF

[Disco](http://elixirforum.com/clicks/track?url=https%3A%2F%2Fgithub.com%2Fdiscoproject%2Fdisco&post_id=641&topic_id=154) is a distributed map-reduce and big-data framework that is similar to Hadoop. It is written in Erlang, but exposes a Python interface; I have not found any Erlang API docs, but it should be feasible to create an Elixir library from it.

### Apache Kafka

[Kafka](http://elixirforum.com/clicks/track?url=http%3A%2F%2Fkafka.apache.org%2F&post_id=641&topic_id=154) is a high-throughput distributed messaging system.

* [KafkaEx](http://elixirforum.com/clicks/track?url=https%3A%2F%2Fgithub.com%2Fkafkaex%2Fkafka_ex&post_id=641&topic_id=154) - someone has dutifully made an Elixir library for Kafka using a binary interface
* [RethinkDB](https://www.rethinkdb.com)

### DOA

    Apache Spark2 - Java or Python interface
    Apache Storm1 - JVM + Clojure DSL; uses Apache Thrift, so non-JVM interfaces are feasible
    Apache Samza2 - JVM + Clojure DSL1; non-JVM support is on the roadmap1
    Apache Flink - JVM-only; example of Clojure implementation1
    
### Highly Distributed File Systems for data

* [HDFS (used by Hadoop)](https://en.wikipedia.org/wiki/Apache_Hadoop#File_systems)
* [Hierarchical Data Format or HDF5](https://www.hdfgroup.org/why_hdf/) (used by many research facilities). It's a standard to work with data spawning on many machines. 
* [netCDF4](http://www.unidata.ucar.edu/software/netcdf/) (a network standard to exchange HDF5 data)

## Experiences and blogposts

* [Defining a micro-services architecture to serve data using standard interfaces (REST)](https://lnkd.in/dwtt5PX)

## Performance

* [Benchmark post of this from some engineers at Yahoo](https://yahooeng.tumblr.com/post/135321837876/benchmarking-streaming-computation-engines-at)
* [Software Engineering Daily podcast talking about the results](http://softwareengineeringdaily.com/2016/02/03/benchmarking-stream-processing-frameworks-with-bobby-evans/)
