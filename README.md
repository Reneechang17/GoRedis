# GoRedis - A Simple Redis Clone in Go

## Project Description

GoRedis is a lightweight, high-performance Redis clone built in Go. The project implements basic Redis-like functionality, including key-value storage, support for multiple clients, and RESP (Redis Serialization Protocol) message handling. The server is capable of accepting multiple concurrent client connections and can handle simple commands such as `SET`, `GET`, `HELLO`, and `CLIENT`. 

## Key Features:

- **Key-Value Storage**: A simple `KV` storage allows clients to perform operations like storing and retrieving key-value pairs efficiently.
- **Multi-Client Support**: Allows multiple clients to connect concurrently, with each client being handled in a separate Goroutine.
- **RESP Protocol**: Supports the Redis Serialization Protocol (RESP), enabling compatibility with Redis-like clients and ensuring proper command and response formatting.
- **TCP-based Communication**: Communication between the server and client is handled over TCP, following the client-server model.
- **Client and Server Implementation**: A simple client that interacts with the server by sending `SET` and `GET` commands, and a server that handles incoming requests.
- **Concurrency and Synchronization**: Uses Go’s Goroutines and channels to manage multiple clients and commands simultaneously.

## Testing:

The project includes several unit tests to ensure that the server and client behave correctly:

1. **Official Redis Client Test**: Verifies that the server works correctly with the official Redis client using basic `SET` and `GET` commands.
2. **Multi-Client Support**: Tests the server's ability to handle multiple concurrent client connections by running multiple clients in parallel.
3. **RESP Protocol Format**: Tests that the server correctly implements the RESP protocol, including generating proper command responses.

## Technical Skills:

- Go, Networking(TCP communication), RESP Protocol, Concurrency(Goroutines and channels)

### References:

- **Go Redis Client**: [github.com/redis/go-redis](https://github.com/redis/go-redis)
- **RESP Implementation in Go**: [github.com/tidwall/resp](https://github.com/tidwall/resp)
- **Redis Protocol Specification**: [Redis Protocol Documentation](https://redis.io/docs/latest/develop/reference/protocol-spec/)
- **Redis HELLO Command**: [Redis HELLO Command Documentation](https://redis.io/docs/latest/commands/hello/)
