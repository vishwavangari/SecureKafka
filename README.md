# SecureKafka
Download Apache Kafka: https://kafka.apache.org/downloads
Navigate to /bin folder in downloaded Kafka binary.

Follow steps in this medium article:
https://medium.com/@vishwateja.vangari/securing-kafka-cluster-using-sasl-acl-and-ssl-dec15b439f9d

Start zookeeper using ./bin/zookeeper-server-start.sh config/zookeeper.properties
and follow below steps before starting Kafka Server

Replace <kafka-binary-dir> with the download path in below files.
server.properties
ssl-user-config.properties
ssl-producer.properties
ssl-consumer.properties

export KAFKA_OPTS=-Djava.security.auth.login.config=<kafka-binary-dir>/config/kafka_server_jaas.conf
./bin/kafka-server-start.sh ./config/server.properties