FROM golang:alpine

RUN apk update \
  && apk add alpine-sdk

COPY ./ /app/backend
WORKDIR /app/backend

RUN go mod init backend \
  && go mod tidy
RUN go build -o backend

CMD ["go", "run", "main.go"]
