# 🦉 OLiteSpeedX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OWeb-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OLiteSpeedX** — OpenLiteSpeed / LiteSpeed Configuration Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OLiteSpeedX is an offline, read-only auditor for OpenLiteSpeed / LiteSpeed configuration (`httpd_config.conf`, vhconf, admin_config). It reviews listeners/TLS, WebAdmin, security, PHP/LSAPI, suEXEC, logging, rewrite, and LSCache settings, plus ownership/permission checks. Secrets are masked; reports export with score/grade to TXT, Markdown, JSON, CSV, or SARIF.

---

## ✨ Features

- Stdlib parser for the LiteSpeed block format, including heredocs
- Listener / TLS, WebAdmin, security section, PHP/LSAPI, suEXEC, disclosure, logging, .htaccess, rewrite, LSCache checks
- Ownership and permission review with optional docRoot content scanning
- Secret masking; CWE + MITRE ATT&CK mapping per finding
- Score and grade; hardened templates via `--template`
- TXT / MD / JSON / CSV / SARIF export, `--demo` self-test, and CI severity gates

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OLiteSpeedX -c /usr/local/lsws/conf --scan
./OLiteSpeedX --root ./collected -f sarif -o litespeed.sarif --fail-on high
./OLiteSpeedX --demo --list-rules
./OLiteSpeedX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
