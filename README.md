# Project README

## Overview
The project is a simple C program that reads input from a PS4 controller and prints actions like button presses to the console.

## Features
- Reads input from a PS4 controller.
- Detects button presses and releases.
- Supports Linux, Windows (via Wine), WebAssembly, and Linux cross compilation for Windows.

## Project Structure
### Prerequisites
- C/C++ Compiler and Debugger (GCC, Clang)
- Make utility
- Standard development tools
- `libudev` library for accessing the PS4 controller (Linux)
- `winetricks` for installing Wine on Linux

## Build & Run
### Building
To build the project:
```bash
cd Cmd_PS4_Controller
make -f Makefile.(os) all
```
Replace `(os)` with your target OS (`linux`, `windows`, `wine`, or `web`).

For a clean rebuild, use:
```bash
make -f Makefile.(os) clean
make -f Makefile.(os) all
```

### Executing
To run the compiled executable:
```bash
make -f Makefile.(os) exe
```
Replace `(os)` with your target OS (`linux`, `windows`, `wine`, or `web`).

For debugging, use:
```bash
make -f Makefile.(os) debug
```

For a web version, run it using Emscripten's runtime:
```bash
wasmtime build/Main.wasm
```