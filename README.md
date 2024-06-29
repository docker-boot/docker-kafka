# Kafka

端口
------
<pre>
9092
</pre>

进容器
------
<pre>
docker-compose exec kafka bash
</pre>

KafkaManager
------
<pre>
http://192.168.31.64:10041
</pre>

查Topic
------
<pre>
kafka-topics.sh --describe --zookeeper 192.168.31.64:2181 --topic topic001
</pre>

查Group
------
<pre>
kafka-consumer-groups.sh --bootstrap-server 192.168.31.64:9092 --list
</pre>

消费消息
------
<pre>
kafka-console-consumer.sh --bootstrap-server 192.168.31.64:9092 --topic topic001 --from-beginning
</pre>

生产消息
------
<pre>
kafka-console-producer.sh --broker-list 192.168.31.64:9092 --topic topic001
kafka-console-producer.sh --broker-list 192.168.31.64:9092 --topic topic001 --property parse.key=true
</pre>
