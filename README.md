flume-ng-kafka-sink
================

This project is used for [flume-ng](https://github.com/apache/flume) to communicate with [kafka 0.7,2](http://kafka.apache.org/07/quickstart.html).

Configuration of Kafka Sink
----------

    agent_log.sinks.kafka.type = com.vipshop.flume.sink.kafka.KafkaSink
    agent_log.sinks.kafka.channel = all_channel
    agent_log.sinks.kafka.zk.connect = 127.0.0.1:2181
    agent_log.sinks.kafka.topic = all
    agent_log.sinks.kafka.batchsize = 200
    agent_log.sinks.kafka.producer.type = async
    agent_log.sinks.kafka.serializer.class = kafka.serializer.StringEncoder


Setup flume
----------
    copy the result jar to lib directory of your flume installation
    copy scala-library-*.jar to lib directory of your flume installation. The library can be found on your local maven repository. under linux is ~/.m2
    copy metrics-core-2.2.0.jar to lib directory of your flume installation
