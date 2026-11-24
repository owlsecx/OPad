# 🦉 OPad

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OCipher-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-orange?style=flat-square"/>
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

This tool is part of the **OwlSec** suite — a collection of 275+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

Proprietary — © 2026 Owlsec LLC. All rights reserved.

*Tools are distributed as pre-built executables. Source code is proprietary.*

---

## 🔍 Verification & Transparency

This tool is closed-source. These files let you see exactly what is inside it,
without the source:

- [`SBOM.cdx.json`](SBOM.cdx.json) — CycloneDX inventory: SHA-256 of this
  binary, bundled CPython version, and every bundled library with its exact
  version and license. Feed it to Grype, Trivy or Dependency-Track to audit
  our dependencies for CVEs yourself.
- [`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md) — the full license text
  of every third-party component, extracted from this binary.

**No telemetry, no analytics, no licence check-in.** This tool does not phone
home. Verify that claim yourself:

```bash
sudo strace -f -e trace=network ./OPad --help   # watch every network call
firejail --net=none ./OPad --help               # deny the network entirely
```

Release signing, GPL compliance and vulnerability reporting:
[**TRUST.md**](https://github.com/owlsecx/owl-os/blob/main/TRUST.md)
