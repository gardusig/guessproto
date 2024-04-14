# guessproto

There are two defined procedures to be remotely called. [Check it out](/proto/guess_service.proto)!

- `GuessNumber`
  - Input: `GuessNumberRequest`
  - Output: `GuessNumberResponse`
- `OpenBox`
  - Input: `LockedBox`
  - Output: `OpenedBox`

## Languages

### Go

#### Install

```
brew install protobuf
brew install protoc-gen-go
brew install protoc-gen-go-grpc
```

#### Generate:

```bash
protoc --go_out=. --go-grpc_out=. proto/guess_service.proto
```

It should generate these files under `/generated/go` folder:

- `guess_service_grpc.pb.go`
- `guess_service.pb.go`
