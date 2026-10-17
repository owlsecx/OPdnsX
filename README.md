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

PowerDNS Authoritative / Recursor / dnsdist configuration hardening auditor

---

## ✨ Features

- Stdlib pdns.conf / recursor.conf (key=value, +=, include-dir) / recursor.yml (YAML-lite) / dnsdist Lua parsers — offline and strictly read-only
- Authoritative — API / webserver exposure, api-key & password strength / hashing, AXFR ACLs, NOTIFY and autoprimary trust, DNS UPDATE ACLs, gmysql / gpgsql / LDAP credentials and TLS, setuid / chroot, Lua records
- Recursor — open resolver ACLs, DNSSEC mode, webserver, API key, cache limits, forward zones, Lua scripts, dont-query / ECS / NXNS mitigations
- dnsdist — setKey strength, controlSocket / console ACL, webserver auth & ACL, frontend ACL, TLS, rate limits
- File ownership / permission checks on configs, include dirs, Lua scripts and backend database files
- Secrets masked everywhere; --root discovery; CWE + MITRE
- Export TXT / Markdown / JSON / CSV / SARIF 2.1.0
- Self-test --demo, CI gates --fail-on / --min-severity

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OPdnsX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
