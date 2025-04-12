
# Beginner's Guide to Collecting Bitz on Eclipse

## What is Bitz?

Collect `$BITZ` by breaking PoW blocks.

---

## Installation Guide

### Prerequisites

- Make sure you have an **Eclipse wallet** set up and funded with **ETH on Eclipse**  
- A computer with terminal access

> **Windows users**: You must first install **WSL** (see Install Dependencies). Then run the following commands inside the **Ubuntu (Linux) terminal**.

---

### Setup Steps

#### Install Rust

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

#### Install Solana CLI

```bash
curl --proto '=https' --tlsv1.2 -sSfL https://solana-install.solana.workers.dev | bash
```

> After installation, add Solana to your `PATH`. The installer will provide instructions.

#### Example Output After Installation

```text
Installed Versions:
Rust: rustc 1.85.0 (4d91de4e4 2025-02-17)
Solana CLI: solana-cli 2.1.14 (src:3ad46824; feat:3271415109, client:Agave)
Anchor CLI: anchor-cli 0.30.1
Node.js: v23.8.0
Yarn: 1.22.1
```

---

### Create a Local Keypair / Wallet

```bash
solana-keygen new
```

> This will create a new keypair at the default location: `~/.config/solana/id.json`

To create it at a custom location:

```bash
solana-keygen new -o /path/to/keypair.json
```

Take note of your **public key** (displayed after generation).

> Eclipse uses `solana-cli`. The ETH balance of your keypair will be shown in **SOL**, but it's actually **Eclipse ETH**.

---

### Set the RPC to Eclipse Mainnet

```bash
solana config set --url https://bitz-000.eclipserpc.xyz/
```

---

### Install Bitz Using Cargo

```bash
cargo install bitz
```

> ⚠️ This might take 5 minutes. It’s normal — wait unless you see an actual error.

---

## Using Bitz

### Fund Your Wallet

Make sure your wallet has a **minimum balance of 0.0005 ETH**.

---

### Basic Commands

- Collect Bitz:
  ```bash
  bitz collect
  ```

- Claim Your Bitz:
  ```bash
  bitz claim
  ```

- Check Your Balance:
  ```bash
  bitz account
  ```

- See All Commands:
  ```bash
  bitz -h
  # or
  bitz --help
  ```

---

## Tips for Beginners

- Run commands regularly to **maximize collection**
- Join the **Eclipse community Discord** for support
