# A Simple 32-bit Calculator Using Rust and WebAssembly

This is a practice project that showcases a Simple Calculator written in Rust. The binary is compiled using **wasm32-unknown-unknown** target and is run using **wasmtime** - A fast a secure runtime for WebAssembly.

## Demo:
```
$ cargo build --target wasm32-unknown-unknown --release
   Compiling calculator v0.1.0 (/home/sidconstructs/Downloads/working/calculator-rust-wasm/calculator)
    Finished release [optimized] target(s) in 0.04s
$ wasmtime ./target/wasm32-unknown-unknown/release/calculator.wasm --invoke add 3 5

8

$ wasmtime ./target/wasm32-unknown-unknown/release/calculator.wasm --invoke sub 3 5

-2

$ wasmtime ./target/wasm32-unknown-unknown/release/calculator.wasm --invoke mul 3 5

15

$ wasmtime ./target/wasm32-unknown-unknown/release/calculator.wasm --invoke div 3 5

0

$ wasmtime ./target/wasm32-unknown-unknown/release/calculator.wasm --invoke div 5 3

1

$ wasmtime ./target/wasm32-unknown-unknown/release/calculator.wasm --invoke div 6 3

2
```
