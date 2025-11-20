# Simple C TCP Server

This is a basic, self-contained TCP server implementation written in **pure C** using standard Linux/Unix sockets programming.

The project demonstrates foundational concepts of network programming, including socket creation, binding, listening, accepting connections, and concurrent handling via `fork()`. The code also includes custom macros and function pointers to create a clean, object-like API for the server and connection structures.

## ✨ Features

  * **Simple API:** Provides an easy-to-use `tcpserver()` function to initialize the server on a specified port.
  * **Concurrency:** Handles multiple incoming client connections concurrently using the `fork()` system call.
  * **Custom Handler:** Allows users to define a custom callback function (`callback cb`) to process connection logic (send/receive).
  * **Encapsulated State:** Uses `server` and `connection` structures with function pointers for basic status (`ok`, `err`) and I/O (`send`, `recv`).
  * **Minimal Dependencies:** Built only with standard C libraries and system headers (like `<sys/socket.h>`).

## ⚙️ Build and Run

### Prerequisites

  * A C compiler (e.g., GCC).
  * The `make` utility.
  * A Unix-like operating system (Linux, macOS, etc.) is required for socket functions and the `fork()` system call.

### Building the Server

The project includes a `Makefile` to simplify the compilation process.

```bash
make
