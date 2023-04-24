FROM postgres:13-alpine

#RUN apk add --no-cache build-base protobuf-c-dev protobuf-c libressl-dev git postgresql-dev

RUN apk add --no-cache build-base protobuf-c-dev protobuf-c git postgresql-dev openssl-dev

RUN git clone https://github.com/debezium/postgres-decoderbufs.git && \
    cd postgres-decoderbufs && \
    make && \
    make install
