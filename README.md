# 🦉 OPdnsX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-ONetwork-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OPdnsX** — PowerDNS Configuration Hardening Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OPdnsX is an offline, read-only configuration auditor for PowerDNS Authoritative, Recursor and dnsdist deployments. It parses their configuration formats and flags hardening issues across APIs, ACLs, DNSSEC, credentials and file permissions. Secrets are masked throughout the output.

---

## ✨ Features

- Parses pdns.conf, recursor.conf/recursor.yml and dnsdist Lua configurations offline
- Audits API/webserver exposure, API-key and password strength, and AXFR/UPDATE ACLs
- Checks Recursor open-resolver ACLs, DNSSEC mode and query mitigations
- Reviews dnsdist console/web ACLs, TLS and rate limits
- File ownership and permission checks with secrets masked everywhere
- Multiple report formats (txt/json/sarif/md/csv), a rule catalogue and hardened templates

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OPdnsX --auth /etc/powerdns/pdns.conf --json -o report.json
./OPdnsX --scan --root /mnt/collected
./OPdnsX --recursor /etc/pdns-recursor/recursor.conf --fail-on high
./OPdnsX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
