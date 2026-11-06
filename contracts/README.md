# Byteforge-Dapp Contracts

Soroban smart contracts workspace used for resource-cost benchmarking, regression verification, and protocol-level testing.

## Structure

```text
contracts/
├── Cargo.toml          # Cargo workspace manifest
├── README.md           # Contracts documentation
└── contract/           # Benchmark and test contract implementation
    ├── Cargo.toml      # Contract package configuration
    ├── Cargo.lock      # Locked dependencies
    └── src/
        └── lib.rs      # Soroban contract entrypoints and test logic
```

## Building Contracts

Verify contracts compile:
```bash
cargo check
```

Build optimized WASM binaries:
```bash
cargo build --target wasm32v1-none --release
```
