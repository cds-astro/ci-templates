# CDS Actions

This repository contains actions that can be useful across the CDS repositories.

## How to use

Let's take the example of `minimal-rust-version-check`. In an other repository, add the
following action:

```yml
name: Check minimal rust version

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  test-old-rust:
    uses: cds-astro/ci-templates/.github/actions/minimal-rust-version-check@main
```

## Content

### minimal-rust-version-check

Installs rustup, get the minimal rust version in Cargo.toml and compiles crate with
this version.