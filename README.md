# ORZ CLI with Nvidia GPU Support

A command line interface for the Orz program to utilize Nvidia GPU's. 


Built by [@BenjaSOL](https://x.com/benjasol_) 

## Building

To build the Orz CLI, you will need to have the Rust programming language installed. You can install Rust by following the instructions on the [Rust website](https://www.rust-lang.org/tools/install).

You must have CUDA installed 

```sh
export CUDA_VISIBLE_DEVICES=<GPU_INDEX>
```

Windows users

```sh
nvcc windows.cu -o windows
```

Linux users

```sh
nvcc linux.cu -o linux
```

Take the path to the executsble that was just created and replace the PATH_TO_EXE with the path to the executable in the src/mine.rs.

Once you have Rust installed, you can build the Orz CLI by running the following command:

```sh
cargo build --release
```


```sh
./target/release/orz.exe --rpc "" --priority-fee 1 --keypair 'path to keypair' --priority-fee 1 mine --threads 4
```

You will now run your hashing on the GPU instead of the CPU!

Donations in ORE, ORZ or SOL: EVK3M6Cth3uPZcATCtnZ16mqArSNXt5oC6kcmakwXudb