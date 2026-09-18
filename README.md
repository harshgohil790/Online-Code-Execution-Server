# Online Code Execution Server

A multi-threaded client-server application built in C using POSIX APIs. It allows clients to submit C or Python code over TCP, executes the code on the server, and returns the output.

## Features

- TCP client-server communication using sockets
- Concurrent client handling using POSIX threads
- C and Python code execution
- Process isolation using `fork()` and `exec()`
- CPU and memory limits using `setrlimit()`
- stdout/stderr capture using pipes
- Timeout-based process termination
- Thread-safe server logging

## Technologies

- C
- POSIX
- TCP Sockets
- pthreads
- Linux/Unix System Calls

## Files

- `server.c` – TCP server and client handling
- `client.c` – Client program for submitting code
- `executor.c` – Code execution and resource management
- `logger.c` – Thread-safe logging
- `server.h` – Shared declarations and configuration

## Build

```bash
gcc server.c executor.c logger.c -o server -pthread
gcc client.c -o client
