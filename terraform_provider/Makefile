provider:
	echo "Building Terraform Provider"

test:
	GO111MODULE=on go test

build:
	GO111MODULE=on go mod tidy
	GO111MODULE=on go build -o terraform-provider-example

clean:
	rm -rf terraform-provider-example

run:
	echo "running ...."


compile:
	echo "Compiling for every OS and Platform"
	GOOS=linux GOARCH=arm go build -o terraform-provider-example 
	GOOS=linux GOARCH=arm64 go build -o terraform-provider-example
	GOOS=freebsd GOARCH=386 go build -o terraform-provider-example

all: provider test build
