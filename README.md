# RISC-V Emulator
Risc-V online emulator with WebAssembly generated by Rust.

The instruction sets in this emulator complies "The RISC-V Instruction Set Manual Volume I: Unprivileged ISA Document Version 20190608-Base-Ratified".

## Build and Run
The `wasm-pack build` command generates a pkg directory and makes Rust source code into `.wasm` binary. It also generates the JavaScript API for using our Rust-generated WebAssembly. The toolchain's supported target is `wasm32-unknown-unknown`.
You need to execute this command whenever you change your Rust code.
```
$ wasm-pack build
```

Use `npm init wasm-app www` just once to generate a www directory for a web page. Also, need `npm install` in a www directory at the first time and whenever you change a dependency in package.json.
```
$ npm init wasm-app www // at a root directory
$ npm install // at ./www directory
```

You can see a web page via http://localhost:8080/ that reflects changes when we rus the wasm-pack build command.
```
$ npm run start
```

## Test
```
$ wasm-pack test --firefox --headless
```

## Tools
- rustup
- rustc
- cargo
- wasm-pack
- cargo-generate
- npm

## Resources
- [Rust and WebAssembly](https://rustwasm.github.io/docs/book/introduction.html)
- [wat2wasm demo](https://webassembly.github.io/wabt/demo/wat2wasm/)
- [RISC-V Software Ecosystem Overview](https://riscv.org/software-status/)
- [RISC-V Online Simulator](https://www.kvakil.me/venus/)
