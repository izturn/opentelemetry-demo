# Checkout Service

This service is a re-implements of checkhoutservice. The different between they are:

- checkhoutservice-v2 doesn't call emailservice
- checkhoutservice-v2 doesn't call currencyservice
- checkhoutservice-v2 doesn't depend kafka

## Local Build

To build the protos and the service binary, run:

```sh
protoc -I ../pb/ ../pb/demo.proto --go_out=./ --go-grpc_out=./
go build -o /go/bin/checkoutservice/ ./
```

## Docker Build

From the root directory, run:

```sh
docker compose build checkoutservice
```
