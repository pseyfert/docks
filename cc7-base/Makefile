.PHONY: all build

REPO := hepsw/cc7-base
TAG := 7

all: build
	@echo "done"

build: Dockerfile
	docker build --rm --tag=$(REPO):$(TAG) .
	docker tag $(REPO):$(TAG) $(REPO):latest

upload: build
	docker push $(REPO):$(TAG)
