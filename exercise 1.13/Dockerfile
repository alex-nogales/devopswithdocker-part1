FROM golang:1.16

EXPOSE 8080

WORKDIR /usr/src/app
RUN apt update 

COPY . .
RUN go build

CMD ["./server"]