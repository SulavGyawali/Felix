# Felix

> A tiny operating system written in Rust — following the "Writing an OS in Rust" tutorial.

## 🧠 Overview

Felix is a from‑scratch operating system built in **Rust**, inspired by and following the structure of the well‑known guide **“Writing an OS in Rust” by Philipp Oppermann**. 

This project explores low‑level system programming, bootloading, memory management, interrupts, VGA text mode output, and eventually multitasking — all without relying on an underlying OS.

It is a learning‑focused project meant to understand how modern kernels work under the hood.


## 🚀 Getting Started

### Prerequisites

- **Rust nightly toolchain**
  ```bash
  rustup override set nightly
  rustup component add rust-src
  ```

- **cargo‑bootimage** (if using bootimage for building ISO)
  ```bash
  cargo install bootimage
  ```

- **QEMU** for virtual machine testing

### Build & Run

Build the OS kernel:
```bash
cargo build
```

Run the OS in QEMU:
```bash
cargo run
```

or if you're using bootimage:
```bash
cargo bootimage
qemu-system-x86_64 -drive format=raw,file=target/x86_64-felix/debug/bootimage-felix.bin
```

## ✨ Features Implemented

- Custom Rust kernel (no standard library)
- Booting via custom bootloader / bootimage
- VGA text mode printing (basic screen output)
- Panic handler

## ⚠️ Notes

This OS is not meant to be production ready. It is an educational project, intended for exploring the fundamentals of kernel and systems development.


