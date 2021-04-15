FROM golang:1.15 as build

ENV PATH $PATH:/usr/local/go/bin
ENV GO111MODULE=on
ENV GOPRIVATE="github.com/mojacon/go"
WORKDIR /mojacon_go

COPY go.mod go.sum ./

RUN set -x \
  && go mod download
COPY . .

RUN set -x \
  && go build

