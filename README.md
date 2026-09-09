> ⚠️**This project has been moved to the main [pnpm](https://github.com/pnpm/pnpm) repository.**

# pacquet

> [!WARNING]
> **pacquet is under active development and not yet ready for production use.**

The official pnpm rewrite in Rust.

pacquet is a port of the [pnpm](https://github.com/pnpm/pnpm) CLI from TypeScript to Rust. It is not a new package manager and not a reimagining of pnpm. Its behavior, flags, defaults, error codes, file formats, and directory layout will match pnpm exactly.

# Pacquet for Android (Termux aarch64)

Pre-compiled native **`pacquet`** binary (Fast Rust-based package manager compatible with pnpm registries) built specifically for **Android aarch64** running inside **Termux**.

Bypass the multi-hour compilation wall and get a lightning-fast package manager running on your phone or tablet instantly.

## Quick Install

Download and extract the pre-compiled binary straight into your local Termux path:
```bash
# 1. Download the release tarball
curl -LO [https://github.com/circyw-ui/pacquet-android-aarch64/raw/main/target/release/pacquet-android-aarch64-termux.tar.gz](https://github.com/circyw-ui/pacquet-android-aarch64/raw/main/target/release/pacquet-android-aarch64-termux.tar.gz)

# 2. Extract the binary
tar -xzvf pacquet-android-aarch64-termux.tar.gz

# 3. Move it to your local bin and make it executable
chmod +x pacquet
mv pacquet $PREFIX/bin/pnpm

# 4. Verify installation
pnpm --version


## Roadmap

pacquet will become the installation engine of pnpm. The transition will happen in two phases.

### Phase 1: fetching and linking

pacquet replaces fetching and linking only. pnpm continues to create the lockfile, and pacquet does the rest. We expect this alone to make pnpm at least twice as fast in most scenarios. Shipping this phase is the current focus.

### Phase 2: resolution

pacquet also takes over dependency resolution.

See [`CONTRIBUTING.md`](./CONTRIBUTING.md) for development setup, debugging, testing, and benchmarking.

## Benchmark

![](https://pnpm.io/img/benchmarks/alotta-files-pnpm.svg)
