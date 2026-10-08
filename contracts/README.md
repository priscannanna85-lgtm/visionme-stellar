# Soroban Contracts

This directory contains the Soroban smart contracts for the project.

## Prerequisites

Install the Stellar CLI and the WebAssembly target:

```bash
cargo install --locked stellar-cli

rustup target add wasm32v1-none
```

## Build

Build all contracts to WebAssembly:

```bash
npm run build
```

This invokes `stellar contract build` and writes the compiled artifacts to `target/wasm32v1-none/release/`.

## Optimize

Optimize the compiled WASM for deployment:

```bash
epm run optimize
```

## Deploy to Testnet

Deploy the optimized contract to Stellar Testnet:

```bash
npm run deploy:testnet
```

The deploy script uses `stellar contract deploy` and reads the WASM from `target/wasm32v1-none/release/`.

## Available Scripts

See `contracts/package.json` for the full list of build, optimize, and deploy scripts.
