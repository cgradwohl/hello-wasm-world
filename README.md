# hello-wasm-world
hello wasm world !


# Install Rust
`curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh`

The toolchain includes:
`rustup` - Rust toolchain manager
`rustc` - Rust Compiler
`cargo` - Rust package manager

# Add WebAssembly as a build target for cargo
`rustup target add wasm32-wasi`

# Create a new Rust project using `cargo`
`cargo new your-new-project-name`

# Build a WebAssembly file using `cargo`
`cargo build --target wasm32-wasi`

Note: Now, in the target folder, there's a hello-world.wasm file.
```
hello-world/
├── Cargo.lock
├── Cargo.toml
├── src
└── target
   └── ...
   └── wasm32-wasi
      └── debug
         └── ...
         └── hello-world.wasm
```

# Install the Wasmtime CLI
`curl https://wasmtime.dev/install.sh -sSf | bash`

Wasmtime is a standalone runtime for WebAssembly.
Wasmtime is a runtime for __executing__ WebAssembly
More info here: https://github.com/bytecodealliance/wasmtime


# Use Wasmtime CLI to execute the `.wasm` file (WebAssembly file)
`wasmtime target/wasm32-wasi/debug/hello-world.wasm`


# How to create a WebAssembly Module
Rust: https://docs.wasmtime.dev/wasm-rust.html
C/C++: https://docs.wasmtime.dev/wasm-c.html
AS: https://docs.wasmtime.dev/wasm-assemblyscript.html
  - https://www.assemblyscript.org/