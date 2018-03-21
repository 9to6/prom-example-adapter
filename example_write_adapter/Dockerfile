FROM golang:latest 
RUN mkdir /app 
ADD . /app/ 
# RUN go install github.com/prometheus/prometheus
RUN go get github.com/prometheus/prometheus/documentation/examples/remote_storage/example_write_adapter
WORKDIR /go/src/github.com/prometheus/prometheus/documentation/examples/remote_storage/example_write_adapter
RUN ls -la
RUN go build -o main .

EXPOSE 1234
ENTRYPOINT ["./main"]
# RUN go build -o main . 
# CMD ["/app/main"]
