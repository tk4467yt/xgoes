FROM golang:1.10-alpine3.7
COPY . /go/tls_client/
RUN cd /go/tls_client && go build 

FROM alpine:3.7
COPY --from=0 /go/tls_client/tls_client /usr/local/bin/tls_client

CMD ["tls_client"]
