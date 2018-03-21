FROM golang:latest 
RUN mkdir /app 
ADD . /app/ 
# RUN go install github.com/prometheus/prometheus
RUN go get github.com/prometheus/prometheus/documentation/examples/remote_storage/remote_storage_adapter
WORKDIR /go/src/github.com/prometheus/prometheus/documentation/examples/remote_storage/remote_storage_adapter
RUN ls -la
RUN go build -o main .

EXPOSE 8080 8081 8086 9201
ENTRYPOINT ["./main"]
# RUN go build -o main . 
# CMD ["/app/main"]
