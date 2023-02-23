# Kafka Server - pvc

### Source: https://github.com/provectus/kafka-ui

1. The code from provectuslabs has a TCP port 8080, to forward it to any port, look at siqi-ui-1.yaml line 9.
2. The KAFKA_CLUSTERS_0_JMXPORT doesn't seem to be needed.
3. KAFKA_CLUSTERS_0_BOOTSTRAPSERVERS should include brokers addresses that specified at KAFKA_ADVERTISED_LISTENERS.
4. KAFKA_BROKER_ID needs to be unique.
5. PLAINTEXT_HOST needs to map to the port section

# Kafka Server - akhq 

### Source: https://akhq.io/docs/

1. source file akhq-1.yaml

#
# To launch a kafka local server: docker-compose -f YAML_FILE.yaml up
# To shut down all containers: docker-compose -f YAML_FILE.yaml down (in a different terminal)
