# GoBookstore

Playground for [go-zero framekwork](https://github.com/zeromicro/go-zero) following [this guide](https://github.com/zeromicro/zero-doc/blob/main/docs/zero/bookstore-en.md)

## Getting started

### Good Reads

- [Rest vs gRPC](https://blog.postman.com/how-to-choose-http-or-grpc-for-your-next-api/)

### Global Dedendencies

- Goctl is a code generation tool based on *.api* files. Run `go install github.com/zeromicro/go-zero/tools/goctl@latest`.
- Run `nano ~/.profile` and add a new line with `export PATH="$HOME/go/bin:$PATH"` to have GoCTL avaiable globally.
- Run `. ~/.profile`.
- To install goctl dependencies Run `goctl env check --install --verbose --force`

## Start a service

- Run `curl -i "http://localhost:8888/check?book=go-zero"`
