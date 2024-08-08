FROM golang:1.17.9-bullseye@sha256:851106cdf6505ffd6f8382971c2d8d47db1386f57f8a1468a8dcd8193d39d14c

RUN apt update && apt install curl git gcc libc-dev

WORKDIR /app

COPY go.mod .
COPY go.sum .

RUN go build -o /bin/abigen github.com/celo-org/celo-blockchain/cmd/abigen
