# Security Policy

This policy applies to all repositories in the Weaver Networks
organisation, including HomeStation and its installer.

## Reporting a vulnerability

**Please do not open a public GitHub issue for security problems.**

Report privately by email: **info@weavernetworks.com**

If you would prefer an alternative channel, say so in a first message with no
technical detail and we will arrange one.

Please include what you found, how to reproduce it, and any impact you have
identified. We will acknowledge receipt within 5 working days and
aim to give a substantive response within 14 days.

## Scope

In scope:

- The HomeStation application — Tauri desktop shell, Axum headless server,
  Svelte frontend
- The `loom` shared core library
- The household Holochain DNA and its zomes
- Install and setup scripts, including the public
  [bootstrap](https://github.com/Weaver-Networks/bootstrap) repository
- Mesh networking configuration (Headscale / Tailscale)
- The local AI inference pipeline, including content safety filtering

Out of scope:

- Upstream dependencies — Ollama, Qdrant, Holochain, Tauri. Report those to
  their own projects. If an upstream issue is made materially worse by how we
  integrate it, that part is in scope and we want to hear about it.
- Findings that require physical access to an unlocked device, or an attacker
  who already has root on the host.

## Supported versions

HomeStation is pre-release software. Security fixes are applied to `main`
only. There is no back-porting to earlier commits at this stage.

## Disclosure

We ask for 90 days from acknowledgement before public disclosure, and will
usually be faster. We will tell you when a fix ships.

Contributors who disclose responsibly are credited in the fix commit and the
release notes, unless they would rather remain anonymous.

## Contact

info@weavernetworks.com

---

*Weaver Networks is registered in England and Wales. Conversion to a
Community Interest Company is in progress.*
