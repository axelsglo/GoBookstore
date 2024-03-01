# GoBookstore

Playground for [go-zero framekwork](https://github.com/zeromicro/go-zero) following [this guide](https://github.com/zeromicro/zero-doc/blob/main/docs/zero/bookstore-en.md)

## Getting started

### Good Reads

- [Rest vs gRPC](https://blog.postman.com/how-to-choose-http-or-grpc-for-your-next-api/)

### Global Dedendencies

- Goctl is a code generation tool based on *.api* files. Run `go install github.com/zeromicro/go-zero/tools/goctl@latest`.
- Run `nano ~/.profile` and add a new line with `export PATH="$HOME/go/bin:$PATH"` to have GoCTL avaiable globally.
- Run `. ~/.profile`.

### VSCode Extensions

- The project comes with recommended extensions for syntax support for `.api` and `.proto` files.

### Create a Go service

- Create a folder with the name of the service you want to create `mkdir apiname`.
- Create an *api* subfolder inside the newly created folder `mkdir apiname/api`.
- Go to the new service folder `cd apiname`.
- To generate the API, run `goctl api -o api/apiname.api`, open the file and assign a title and a description to it.
- To generate Go code with a service based off an existing API, run `goctl api go -api api/apiname.api -dir .`, the service will have the same name as the API.
- Run `go mod tidy` to install all of the service dependencies.
- To install goctl missing dependencies if necessary, run `goctl env check --install --verbose --force`

### Run a service

- To start the service run `go run go/servicename.go -f go/etc/servicename-api.yaml`.
- Run `curl -i "http://localhost:8888/endpointname?param=value"`

### Run the bookstore service

- To start the service run `go run go/bookstore.go -f go/etc/bookstore-api.yaml`.
- Run `curl -i "http://localhost:8888/check?book=go-zero"`
