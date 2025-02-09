# Go HTTP Request Logger

This is a simple Go program that makes an HTTP GET request to [Google](http://google.com) and logs the response body while implementing a custom writer.

## Features

- Makes an HTTP request to `http://google.com`
- Uses a custom `logWriter` to print the response body and the number of bytes written
- Demonstrates implementing the `io.Writer` interface in Go

## Prerequisites

- Go installed on your system (download from [golang.org](https://golang.org/dl/))

## How It Works

1. The program sends an HTTP GET request to `http://google.com`.
2. If the request fails, it prints the error and exits.
3. It defines a custom `logWriter` type that implements the `io.Writer` interface.
4. The `Write` method of `logWriter` prints the response body and logs the number of bytes received.
5. The response body is copied to the custom writer using `io.Copy()`.

## Running the Program

To run the program, use:

```sh
go run main.go
```
