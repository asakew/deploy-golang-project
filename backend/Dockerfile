FROM golang:1.23-alpine AS builder

WORKDIR /app

COPY go.mod go.sum ./
RUN go mod download

COPY ./internal ./internal
COPY ./app ./app

RUN go build -o /backend ./app

EXPOSE 3000

CMD [ "/backend" ]
