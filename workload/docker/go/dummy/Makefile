.PHONY: all build clean

CURRENT_DIR := $(shell pwd)
OUTPUT_DIR := $(shell pwd)/bin

all: build
	docker compose build

build:
	GOOS=linux go build -o $(OUTPUT_DIR)/start \
	$(CURRENT_DIR)/src/start.go

clean:
	rm -rf $(OUTPUT_DIR)
