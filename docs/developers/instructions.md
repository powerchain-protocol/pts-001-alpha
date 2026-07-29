# Developer Instructions

**Document ID:** PTS-DEV-001
**Title:** Developer Instructions
**Version:** 1.0.0 Alpha
**Status:** Experimental Alpha Release
**Category:** Informative
**Organization:** PowerChain Standards Organization (PSO)

---

# Purpose

This document provides guidance for developers contributing to the **PowerChain Programmable Asset Token Standard (PTS-001)**.

It explains the recommended development workflow, repository layout, coding standards, testing expectations, and release process.

---

# Repository Structure

```text
PTS-001-ALPHA/

├── docs/
├── specification/
├── scripts/
├── sdk/
├── protobuf/
├── openapi/
├── schemas/
├── registries/
├── reference-implementation/
├── test-vectors/
├── certification/
├── examples/
│
├── README.md
├── CONTRIBUTING.md
├── SECURITY.md
├── LICENSE
└── package.json
```

---

# Development Environment

Recommended tools:

* Git
* Node.js (LTS)
* npm
* Docker (optional)
* Protocol Buffers compiler (`protoc`)
* OpenAPI tooling
* Markdown editor with linting support

---

# Initial Setup

Clone the repository:

```bash
git clone https://github.com/<organization>/PTS-001-ALPHA.git
cd PTS-001-ALPHA
```

Install project dependencies:

```bash
npm install
```

---

# Useful Scripts

Run common tasks from the repository root:

```bash
./scripts/bootstrap.sh
./scripts/build.sh
./scripts/lint.sh
./scripts/validate.sh
./scripts/test.sh
```

Additional scripts:

```bash
./scripts/package.sh
./scripts/release.sh
./scripts/generate-docs.sh
./scripts/generate-openapi.sh
./scripts/generate-protobuf.sh
./scripts/generate-schemas.sh
```

---

# Coding Standards

Developers should:

* Follow language-specific style guides.
* Keep code modular and well documented.
* Write descriptive commit messages.
* Prefer backward-compatible changes.
* Avoid introducing breaking changes during the Alpha phase unless clearly documented.

---

# Documentation

Documentation should:

* Use Markdown.
* Include the standard metadata header.
* Clearly distinguish **Normative**, **Informative**, and **Reference** content.
* Update examples when protocol behavior changes.

---

# Specifications

Changes affecting protocol behavior must also update:

* `specification/PTS-001-alpha.md`
* OpenAPI definitions
* Protocol Buffer definitions
* JSON Schemas
* Test vectors

---

# Testing

Every functional change should include:

* Unit tests
* Validation tests
* Schema validation
* Documentation review

Where applicable, verify interoperability across supported profiles.

---

# Conformance

Implementations should validate:

* Asset identifiers
* Metadata
* Lifecycle transitions
* Registry operations
* Event formats
* Digital signatures

---

# Branching Strategy

Suggested branches:

* `main` — Stable development branch
* `develop` — Ongoing integration
* `feature/<name>` — New features
* `bugfix/<name>` — Bug fixes
* `release/<version>` — Release preparation

---

# Pull Requests

Before opening a pull request:

* Rebase onto the latest development branch.
* Ensure tests pass.
* Update documentation.
* Add or update examples if behavior changes.
* Describe the purpose and scope of the change.

---

# Security

Do not commit:

* Private keys
* Secrets
* API tokens
* Credentials
* Sensitive production data

Security issues should follow the process described in `SECURITY.md`.

---

# Release Process

For each release:

1. Update the specification.
2. Update documentation.
3. Regenerate schemas and Protocol Buffers.
4. Validate OpenAPI definitions.
5. Run the full test suite.
6. Update `CHANGELOG.md`.
7. Tag the release.

---

# Versioning

PTS-001 follows Semantic Versioning.

Current release:

```text
1.0.0 Alpha
```

Future milestones:

* 1.0.0 Beta
* 1.0.0 Stable

---

# Experimental Status

PTS-001 Alpha is an experimental specification.

Expect:

* API changes
* Schema updates
* Additional protocol profiles
* Expanded SDK support
* Refinements based on community feedback

Breaking changes may occur before the Beta release.

---

# Getting Help

If you have questions:

* Review the documentation in `/docs`.
* Read the core specification in `/specification/PTS-001-alpha.md`.
* Check existing issues and discussions before opening new ones.

---

# Related Documents

* `README.md`
* `CONTRIBUTING.md`
* `SECURITY.md`
* `CHANGELOG.md`
* `docs/README.md`
* `specification/PTS-001-alpha.md`

---

**PowerChain Standards Organization (PSO)**
**Developer Instructions**
**Version 1.0.0 Alpha — Experimental Alpha Release**
