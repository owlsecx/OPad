# 🦉 OPad

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OCipher-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0-cyan?style=flat-square"/>
</p>

> **OPad** — One-Time Pad & Vernam Cipher

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OPad implements one-time pad / Vernam XOR cryptography: generate CSPRNG OTP keys, encrypt/decrypt text or files, analyse key entropy, and support multi-format I/O. CLI helpers generate N random key bytes (hex or base64) and analyse a key file's entropy/quality as JSON. Correct OTP use requires a random, secret, never-reused key at least as long as the message.

---

## ✨ Features

- Generate cryptographically secure OTP key bytes via CSPRNG (`--genkey N`)
- Output encoding for generated keys: hex or base64 (`--format`)
- Analyse a key file's entropy/quality and print JSON (`--analyze`)
- Vernam XOR encrypt/decrypt for text and files in the interactive workflow
- Key entropy analysis (Shannon, chi-squared) and XOR secret sharing helpers
- HMAC-SHA256 integrity tags and clipboard / output-directory support in the full UI

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OPad --genkey 32 --format hex
./OPad --genkey 64 --format b64
./OPad --analyze key.bin
./OPad --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
