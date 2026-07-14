# Contributing

Thanks for your interest in contributing to Stellar Invoice Protocol!

Setup

1. Install Rust (nightly is *not* required; stable is fine):
   - https://rustup.rs/
2. Add the wasm32 target for contract builds:
   - `rustup target add wasm32-unknown-unknown`
3. Install the Soroban / Stellar CLI toolchain per Stellar/Soroban docs if you want to use `stellar contract build` and `stellar contract deploy`.

Running tests locally

- Unit tests use `soroban-sdk`'s test utilities. Run:

```
cargo test
```

Building the contract wasm

- With soroban CLI (recommended):
  - `stellar contract build`
- Or with cargo directly:
  - `cargo build --target wasm32-unknown-unknown --release`

Submitting a PR

- Branch naming: use descriptive kebab-case, e.g. `feature/add-invoice-batch-api` or `fix/handle-overflow`.
- Commit style: keep commits focused; use conventional messages like `feat: add invoice index by payer` or `fix: prevent overpayment`.
- Open a PR and link it to an issue if applicable. Include tests and update README/CHANGELOG where relevant.

Code style

- Keep code idiomatic Rust and lean on `soroban-sdk` patterns.
- Add unit tests for all behavior changes and ensure `cargo test` passes.

Thanks!
