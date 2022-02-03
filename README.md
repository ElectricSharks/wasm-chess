# WASM-CHESS

## What is it?
This library is a basic implementation of a chess min-max algorithm with alpha-beta
pruning ([Algorithm Info](https://en.wikipedia.org/wiki/Alpha%E2%80%93beta_pruning)). It is designed to be compiled down to WebAssembly and used for web applications.

## How strong is it?
Honestly, it's not very strong. The algorithm is currently designed to evaluate positions based on piece count, whether it's checkmate, and the number of pieces a player has on the central four squares (the latter being treated as an order of magnitude less important).

The algorithm does not currently use an opening book, nor does it possess an endgame tablebase. These are features that I may add at a later date.

## How do I use it?
To build the WebAssembly version, first ensure that you have cargo installed. Then install wasm-pack via:
```
cargo install wasm-pack
```
Once you have installed wasm-pack, navigate to the root directory and run:
```
wasm-pack build --target web
```
The output is contained in the newly created pkg directory.

## How do I run the UTs?
```
cargo test
```