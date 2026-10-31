# Osprey Peek

![An osprey holding a fish](https://gitlab.com/fmarsault/osprey-peek/-/raw/main/assets/brand/hero-1440.jpg)

**Peek into object storage. Don't download it.**

This repository is a pointer. The app, its source, its releases and its issues live on
GitLab: **https://gitlab.com/fmarsault/osprey-peek**

Osprey Peek is a macOS app that opens a Parquet, CSV or text file in S3, or on disk, and
shows it in place: a storage tree, a data grid, and what the read will cost before it
starts. A Parquet preview reads the footer and then only the row groups you look at; a
text file costs one 128 KiB ranged read. Nothing is ever written to your bucket.

- **Source and documentation** — https://gitlab.com/fmarsault/osprey-peek
- **Download (macOS 13+, arm64 / amd64)** — https://gitlab.com/fmarsault/osprey-peek/-/releases/latest
- **Issues** — https://gitlab.com/fmarsault/osprey-peek/-/issues
- **Security reports** — a confidential issue: https://gitlab.com/fmarsault/osprey-peek/-/issues/new?issue%5Bconfidential%5D=true

Unzip the download, drag `Osprey Peek.app` to Applications, then clear the quarantine
flag once — the app is unsigned for now:
`xattr -d com.apple.quarantine "/Applications/Osprey Peek.app"`

The app never asks for, stores or writes a key: it uses the AWS chain already on the
machine, and it has no write path. MIT licensed.
