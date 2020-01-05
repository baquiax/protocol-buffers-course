# protocol-buffers-course
Examples and exercise of the Protocol Buffers course

## Protoc

To compile the `proto` files, you need to have installed the `protoc`ompiler.

Here you can get the last version of the source code: `https://github.com/protocolbuffers/protobuf/releases`

An example of how to install it is here:

```
# Make sure you grab the latest version
curl -OL https://github.com/google/protobuf/releases/download/v3.5.1/protoc-3.5.1-linux-x86_64.zip
# Unzip
unzip protoc-3.5.1-linux-x86_64.zip -d protoc3
# Move protoc to /usr/local/bin/
sudo mv protoc3/bin/* /usr/local/bin/
# Move protoc3/include to /usr/local/include/
sudo mv protoc3/include/* /usr/local/include/
# Optional: change owner
sudo chown [user] /usr/local/bin/protoc
sudo chown -R [user] /usr/local/include/google
```

### Compiling

In go you ned to have installed this mod 

```
go get -u github.com/golang/protobuf/protoc-gen-go
```

and configured your `$GOPATH/bin` in the `$PATH` env var.

`protoc --proto_path=. --go_out=output person.proto`