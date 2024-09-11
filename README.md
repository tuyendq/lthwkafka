# LTHW - Apache Kafka

## Kafka components
- Producers 
- Consumers 
- Topics 

## Kafka architecture
- Kafka servers / brokers
- Kafka clients 


```bash

bin/kafka-topics.sh --help
bin/kafka-topics.sh --version
# List topics
bin/kafka-topics.sh --bootstrap-server localhost:9092 --list

# Create topic
bin/kafka-console-producer.sh --bootstrap-server localhost:9092 --topic topic-name-here --create

# Delete topic (all messages are deleted too)
bin/kafka-console-producer.sh --bootstrap-server localhost:9092 --topic topic-name-here --delete

# Write
echo "This is a test message" | 
bin/kafka-console-producer.sh --bootstrap-server localhost:9092 --topic topic-name-here

# Read
bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic phishing-sites --from-beginning

bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic phishing-sites --from-beginning --max-messages 3

```

```bash
# to find the number of brokers in the cluster
/home/repl/check_broker.sh

```