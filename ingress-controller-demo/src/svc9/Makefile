
#
## usage:
#    make build repos=xxxx tag=v0.1
#    #

# default

repos=docker.io/bigwhite/ingress-controller-demo-svc9
tag=v0.1

all: push

build:
	go build -o svc9 main.go

buildimage: build 
	docker build -t $(repos):$(tag) .

push: buildimage
	docker push $(repos):$(tag)

pull:
	docker pull $(repos):$(tag)

test:
	go test -v ./...
