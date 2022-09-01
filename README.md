**[Portuguese version](./README_pt_br.md)** 

# POC - Kafka + Golang

Golang application to test kafka connections.

## Docker


## Kafka









## TESTS

**Kafa commands:**

1 - First step enter the container:

```sh
docker exec -it kafka bash
```

2- Some commands for testing with kafka:

```sh
kafka-topics --create --topic=test --bootstrap-server=localhost:9092 --partitions=3

kafka-topics --list --bootstrap-server localhost:9092

kafka-topics  --bootstrap-server=localhost:9092 --topic=test --describe

kafka-console-consumer --bootstrap-server=localhost:9092 --topic=test 

kafka-console-producer --bootstrap-server=localhost:9092 --topic=test

kafka-console-consumer --bootstrap-server=localhost:9092 --topic=test --from-beginning
```

Consumer group for each one to work on reading the partitions:

>> add to command line —group=<GROUP NAME>


**GoLang Consumer command:**

```sh
docker exec gokafka-app go run cmd/consumer/main.go
```

**GoLang Produce command:**

```sh
docker exec gokafka-app go run cmd/producer/main.go
```

