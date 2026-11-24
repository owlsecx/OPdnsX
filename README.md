# 🦉 OPdnsX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-ONetwork-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-orange?style=flat-square"/>
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
sudo strace -f -e trace=network ./OPdnsX --help   # watch every network call
firejail --net=none ./OPdnsX --help               # deny the network entirely
```

Release signing, GPL compliance and vulnerability reporting:
[**TRUST.md**](https://github.com/owlsecx/owl-os/blob/main/TRUST.md)
