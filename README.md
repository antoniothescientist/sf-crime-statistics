# SF crime statistics

In this project, the Kaggle dataset on San Francisco crime incidents is used for statistical analysis using Apache Spark Structured Streaming. A Kafka server is used to produce data, and data is ingested through Spark Structured Streaming.

## Running the project

Start Zookeeper, Kafka server, and Kafka bootstrap server using the following command:

`bin/zookeeper-server-start.sh config/zookeeper.properties`
`bin/kafka-server-start.sh config/server.properties`

To make sure that the the producer_server.py file is running correctly, run the default consumer:

`./bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic call-center --from-beginning`


## Create and run the `consumer_server.py`

Run `consumer_server.py` to consume data produced from the kafka producer.

## Spark submit and run data_stream.py

Run spark submit using the command below:

`spark-submit --packages org.apache.spark:spark-sql-kafka-0-10_2.11:2.3.0 --master local[4] data_stream.py`

then run 

`data_stream.py`

## Run producer_server.py

Check if the producer_server.py is correctly implemented by running:

`bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic call-centre --from-beginning`
