FROM golang:1.15.6-alpine@sha256:f467abead5705eaeadc939ad11cfe85c73650349b8663aaf354f7a9d8f437132

RUN apk add curl git gcc libc-dev linux-headers

WORKDIR /app

COPY go.mod .
COPY go.sum .

RUN go build -mod=readonly -o /bin/abigen github.com/ethereum/go-ethereum/cmd/abigen
