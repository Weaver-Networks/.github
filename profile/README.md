# Weaver Networks CIC

**Cooperative, community-owned AI infrastructure.**  
UK Community Interest Company · No. 15295867 · [weaver-networks.com](https://weaver-networks.com)

---

## What we build

**[HomeStation](https://github.com/Weaver-Networks/homestation)** — a local AI node on refurbished hardware. Your documents stay on your machine. Your queries stay private. When you choose to share, only vector embeddings travel — never raw content. Runs on hardware you own, inside a cooperative you govern.

**[Shutl.ing](https://shutl.ing)** — cooperative GPU infrastructure. Overflow compute and coordination services for the commons tier. CIC-owned, asset-locked, cannot be extracted.

Both are mission-locked inside a CIC asset lock. The commons cannot be sold, acquired, or extracted. That is structural, not policy.

---

## The stack works. Here is what it does.

A HomeStation node today:

- Runs local AI inference via Ollama (no cloud, no API keys, no data leaving your machine)
- Indexes your documents with semantic vector search (Qdrant + MiniLM embeddings)
- Screens content via llama-guard3 before and after inference
- Connects to an encrypted WireGuard mesh (Headscale, self-hosted)
- Participates in a governed distributed inference commons (Petals, private CIC swarm)
- Has a cryptographic identity placeholder on a Holochain source chain — conductor integration in active development

This is not a roadmap. It runs on refurbished Dell hardware across three active dev and operator nodes today.

---

## The one remaining gap

The Headscale mesh coordinator, Kitsune2 Holochain bootstrap server, Petals DHT bootstrap peer, and community Qdrant instance currently run on a DigitalOcean droplet. That is a deliberate, known, temporary dependency — commercial cloud infrastructure coordinating a supposedly sovereign mesh.

When Shutl.ing reaches operational capacity on CIC-owned physical hardware, those services migrate. At that point every layer of the stack — inference, identity, search, mesh coordination, peer bootstrap, governance — runs on asset-locked cooperative infrastructure. Nothing touches commercial cloud.

**That is the sovereignty circle closing. Funding Shutl.ing closes it.**

---

## The ecosystem we're part of

Weaver is infrastructure within the [Holochain](https://holochain.org) ecosystem — building the hardware and governance layer that the network needs but doesn't yet have.

```
Holochain (framework)
  └── Flowsta (sovereign identity — W3C DID on Holochain DHT)
        └── Weaver CIC onboarding (community membership, KYC, governance)
              └── HomeStation node (local AI + mesh + Holochain conductor)
                    ├── Holo Edge Node (always-on network contribution)
                    ├── ZeroClaw agent (ambient AI access via messaging apps)
                    ├── Petals commons tier (distributed inference, governed swarm)
                    └── HoloPort enrolment (hosting marketplace, HoloFuel)
                          └── Unyt accounting (P2P value flow across all layers)
```

Every layer in that tree is a relationship, not just a dependency. We build on these projects, contribute back to them, and depend on each other succeeding.

---

## Our upstream relationships

### 🧬 [holochain/holochain](https://github.com/holochain/holochain)
The root. Agent-centric distributed applications with no global consensus overhead. HomeStation nodes run a Holochain conductor. Identity, governance accountability, and proof-of-service accounting all live on Holochain source chains.

### 🪪 [WeAreFlowsta/flowsta-identity-dna](https://github.com/WeAreFlowsta/flowsta-identity-dna)
Sovereign identity for the Holochain ecosystem. Every HomeStation member gets a W3C-compliant DID generated locally on their device, registered on Flowsta's censorship-resistant public DHT. Flowsta answers *who you are cryptographically*. Weaver CIC onboarding answers *who you are to this community*. We also provide the community-run Edge Node hardware that Flowsta's own sovereignty roadmap requires.

### 🌐 [Holo-Host/edgenode](https://github.com/Holo-Host/edgenode)
The container that turns any hardware into an always-on Holochain node. HomeStation nodes optionally enrol as Holo Edge Nodes after CIC onboarding, contributing DHT gossip and hApp hosting under their verified Flowsta DID.

### 🦀 [zeroclaw-labs/zeroclaw](https://github.com/zeroclaw-labs/zeroclaw)
A lightweight Rust agent runtime (~5MB) that gives HomeStation nodes a conversational AI interface accessible from any messaging app — Telegram, Signal, WhatsApp — over the encrypted mesh. Your private AI assistant on your phone, running on your own hardware.

### 🌸 [bigscience/petals](https://github.com/bigscience-workshop/petals)
Distributed transformer inference across consumer GPUs. We run a private Petals swarm among verified CIC member nodes. We have contributed patches for `hivemind` compatibility with `torch 2.4+` and documented the full dependency conflict chain. We also built what Petals never had: an economic layer. Proof-of-service logging, mutual credit via Unyt, Holochain agent key pairing to node identity, and CIC membership as the Sybil-resistance membrane.

---

## Where we are

| Milestone | Status |
|-----------|--------|
| Local AI inference (Ollama, Llama 3.1/3.2, llama-guard3) | ✅ Done |
| Semantic document search (Qdrant + MiniLM) | ✅ Done |
| Encrypted mesh networking (Headscale/WireGuard) | ✅ Done |
| Governed Petals inference swarm (CIC member nodes) | ✅ Done |
| `hivemind` torch 2.4+ patch — upstream PR opened | ✅ Done |
| Dependency conflict chain — upstream issue documented | ✅ Done |
| Wind Tunnel runner participation (NUC, isolated container) | ✅ Done |
| Holo Edge Node running on HomeStation hardware (Requests & Offers alpha) | ✅ Done |
| Flowsta DID integration — conductor + identity tab | 🔄 Active sprint |
| Holochain conductor wire-in (Lair keystore, source chain) | 🔄 Active sprint |
| Per-node authentication (agent key replaces shared API key) | 🔄 Active sprint |
| ZeroClaw ambient agent (mesh-accessible AI via Signal/Telegram) | 📋 Next |
| Unyt wallet + compute accounting | 📋 Next |
| CIC web onboarding (browser-based T&Cs + membership) | 📋 Next |
| Shutl.ing physical infrastructure — DO droplet migration | 🎯 Funding target |

---

## Principles

**You cannot found a commons on debt — it must be built on fair, sustainable contribution.**

- **Privacy by architecture, not policy.** Data stays on your hardware structurally. We can't surveil you because the architecture doesn't permit it — not because we promise we won't.
- **Underpromise, overdeliver.** We do not hype or sell a dream. We show you what works, name what doesn't yet, and ask you to help build the next piece.
- **The commons is governed, not open.** CIC membership carries responsibilities. Ostrom principles apply. Accountability is structural.
- **Circular at every layer.** Refurbished hardware. 9-10 year lifecycles vs the 4-year industry standard. Extracting useful life rather than manufacturing demand.
- **Extraction-free is viable.** 60%+ gross margins. Zero shareholder extraction. Every pound of profit serves the mission.

---

## Repos

| Repo | What it is |
|------|-----------|
| [homestation](https://github.com/Weaver-Networks/homestation) | Core HomeStation stack — Flask dashboard, Ollama inference, Qdrant vector search, Headscale mesh |
| [.github](https://github.com/Weaver-Networks/.github) | Org profile and community health files |

---

## Team

**Sam Turner** — Founder, Operational Lead & Strategy · Colchester, UK  
**Eric Verkleij** — Co-director · Netherlands  
**Heikki Cabrera** — Co-director · Finland  
**Michiel van Dijk** — Co-director · Netherlands

---

## Partners

[Holochain Foundation](https://holochain.org) · [Flowsta](https://flowsta.com) · [Holo Hosting](https://holo.host) · [Unyt Accounting Ltd](https://unyt.earth) · [Bluetron](https://bluetron.eu) · Dell Refurbished

---

*The stack works. Help us own the last piece.*  
