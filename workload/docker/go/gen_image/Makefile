.PHONY: all build clean

CURRENT_DIR := $(shell pwd)
OUTPUT_DIR := $(shell pwd)/bin
PROJ_NAME := $(shell basename $(CURRENT_DIR))

all: build
	docker compose build

start:
	GOOS=linux go build -o $(OUTPUT_DIR)/start \
	$(CURRENT_DIR)/src/start.go

build: start demo

demo:
	go build -o $(OUTPUT_DIR)/demo \
	$(CURRENT_DIR)/src/demo.go

clean:
	rm -rf $(OUTPUT_DIR)

.PHONY: all build clean demo
