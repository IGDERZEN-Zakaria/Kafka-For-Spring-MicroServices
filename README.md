# Kafka-For-Spring-MicroServices

## Installing Kafka
check this link
https://kafka.apache.org/quickstart


## Creating the project 

![pic01.png](images%2Fpic01.png)

![pic02.png](images%2Fpic02.png)

### Reading events with Kafka script 

get inside Kafka directory and execute this commande to display the topic data

```
bin/kafka-console-consumer.sh --topic "Topic_Name" --from-beginning --bootstrap-server localhost:9092

bin/kafka-console-consumer.sh --topic amigoscode --from-beginning --bootstrap-server localhost:9092
```

# Troubleshooting

![Conversion error.png](images%2FConversion%20error.png)![Conversion.png](images%2FConversion.png)

add this Bean to the consumerConfig class
```
    @Bean
    public RecordMessageConverter converter() {
        return new JsonMessageConverter();
    }
```