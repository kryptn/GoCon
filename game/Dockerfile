from golang:1.7-alpine

env GOBIN /go/bin

run apk --update add git

copy src /go/src

run cd src \
 && go get \
 && go build conway.go \
 && mv conway ../bin

cmd ["sh", "-c", "/go/bin/conway"]
