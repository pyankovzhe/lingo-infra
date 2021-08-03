
# Infrastructure repository of Lingo project

## Kafka

#### Create topic with partitions

```sh
/opt/bitnami/kafka/bin/kafka-topics.sh --create --zookeeper zookeeper:2181 --topic accounts --partitions 1 --replication-factor 1
```

#### Describe topic

```sh
/opt/bitnami/kafka/bin/kafka-topics.sh --describe --zookeeper zookeeper:2181 --topic accounts
```

#### Run console producer
```sh
/opt/bitnami/bin/kafka-console-producer.sh --topic accounts --bootstrap-server kafka:9092
```

#### Run console consumer
```sh
/opt/bitnami/bin/kafka-console-consumer.sh --topic accounts --partition 0 --from-beginning --bootstrap-server kafka:9092
```
