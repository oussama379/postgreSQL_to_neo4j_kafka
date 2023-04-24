FROM debezium/connect:latest

ENV KAFKA_CONNECT_AVRO_CONVERTER_VERSION=5.5.0
ENV CLASSPATH=$CLASSPATH:/kafka/connect/plugins/*

RUN mkdir -p /kafka/connect/plugins && \
    chmod -R 777 /kafka/connect/plugins && \
    curl -sSL https://packages.confluent.io/maven/io/confluent/kafka-connect-avro-converter/${KAFKA_CONNECT_AVRO_CONVERTER_VERSION}/kafka-connect-avro-converter-${KAFKA_CONNECT_AVRO_CONVERTER_VERSION}.jar --output /kafka/connect/plugins/kafka-connect-avro-converter.jar && \
    curl -sSL https://packages.confluent.io/maven/io/confluent/kafka-connect-avro-data/${KAFKA_CONNECT_AVRO_CONVERTER_VERSION}/kafka-connect-avro-data-${KAFKA_CONNECT_AVRO_CONVERTER_VERSION}.jar --output /kafka/connect/plugins/kafka-connect-avro-data.jar && \
    curl -sSL https://packages.confluent.io/maven/io/confluent/kafka-schema-registry-client/${KAFKA_CONNECT_AVRO_CONVERTER_VERSION}/kafka-schema-registry-client-${KAFKA_CONNECT_AVRO_CONVERTER_VERSION}.jar --output /kafka/connect/plugins/kafka-schema-registry-client.jar && \
    curl -sSL https://packages.confluent.io/maven/io/confluent/kafka-schema-registry/${KAFKA_CONNECT_AVRO_CONVERTER_VERSION}/kafka-schema-registry-${KAFKA_CONNECT_AVRO_CONVERTER_VERSION}.jar --output /kafka/connect/plugins/kafka-schema-registry.jar && \
    curl -sSL https://packages.confluent.io/maven/io/confluent/kafka-avro-serializer/${KAFKA_CONNECT_AVRO_CONVERTER_VERSION}/kafka-avro-serializer-${KAFKA_CONNECT_AVRO_CONVERTER_VERSION}.jar --output /kafka/connect/plugins/kafka-avro-serializer.jar && \
    curl -sSL https://packages.confluent.io/maven/io/confluent/kafka-schema-serializer/${KAFKA_CONNECT_AVRO_CONVERTER_VERSION}/kafka-schema-serializer-${KAFKA_CONNECT_AVRO_CONVERTER_VERSION}.jar --output /kafka/connect/plugins/kafka-schema-serializer.jar && \
    curl -sSL https://packages.confluent.io/maven/io/confluent/common-config/${KAFKA_CONNECT_AVRO_CONVERTER_VERSION}/common-config-${KAFKA_CONNECT_AVRO_CONVERTER_VERSION}.jar --output /kafka/connect/plugins/common-config-${KAFKA_CONNECT_AVRO_CONVERTER_VERSION}.jar && \
    curl -sSL https://packages.confluent.io/maven/io/confluent/common-utils/${KAFKA_CONNECT_AVRO_CONVERTER_VERSION}/common-utils-${KAFKA_CONNECT_AVRO_CONVERTER_VERSION}.jar --output /kafka/connect/plugins/common-utils-${KAFKA_CONNECT_AVRO_CONVERTER_VERSION}.jar && \
    curl -sSL https://repo1.maven.org/maven2/org/apache/avro/avro/1.8.2/avro-1.8.2.jar --output /kafka/connect/plugins/avro-1.8.2.jar && \
    curl -sSL https://repo1.maven.org/maven2/org/codehaus/jackson/jackson-core-asl/1.9.13/jackson-core-asl-1.9.13.jar --output /kafka/connect/plugins/jackson && \
    curl -sSL https://repo1.maven.org/maven2/org/codehaus/jackson/jackson-core-asl/1.9.13/jackson-core-asl-1.9.13.jar --output /kafka/connect/plugins/jackson-core-asl-1.9.13.jar && \
    curl -sSL https://repo1.maven.org/maven2/org/codehaus/jackson/jackson-mapper-asl/1.9.13/jackson-mapper-asl-1.9.13.jar --output /kafka/connect/plugins/jackson-mapper-asl-1.9.13.jar
