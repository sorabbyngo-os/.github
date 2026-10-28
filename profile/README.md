<p align="center">
  <img src="https://raw.githubusercontent.com/sorabbyngo-os/.github/main/assets/org-banner.svg" alt="Sorabbyngo OS: an independent, AI-native Linux system" width="100%">
</p>

<p align="center">
  <img alt="Base: Linux 6.19" src="https://img.shields.io/badge/kernel-Linux%206.19-AA66FF?style=for-the-badge&labelColor=080608">
  <img alt="Base: Fedora bootc" src="https://img.shields.io/badge/base-Fedora%20bootc-6C3FC4?style=for-the-badge&labelColor=080608">
  <img alt="Language: Rust" src="https://img.shields.io/badge/core-Rust-FF6B35?style=for-the-badge&labelColor=080608">
  <img alt="Status: pre-alpha" src="https://img.shields.io/badge/status-pre--alpha-FF6B35?style=for-the-badge&labelColor=080608">
</p>

<p align="center">
  <a href="#what-is-sorabbyngo-os">What it is</a> ·
  <a href="#how-the-pieces-fit">How it fits</a> ·
  <a href="#the-repositories">Repositories</a> ·
  <a href="#where-to-start">Where to start</a> ·
  <a href="#contributing">Contributing</a>
</p>

<p align="center"><img src="https://raw.githubusercontent.com/sorabbyngo-os/.github/main/assets/divider.svg" alt="" width="100%"></p>

## What is Sorabbyngo OS?

Sorabbyngo OS is an independent Linux system where intelligence is **infrastructure, not a chatbot**.

You can talk to it, type to it, or ignore the AI completely. Every path ends at the same mediated, observable, undoable action API, and the system always works without a model.

Four ideas shape everything in this organization:

- **Intelligence is optional.** The desktop never blocks on a model, and the direct path (mouse, keyboard, touch) is always complete.
- **One mediated door.** AI has no private powers. It acts through the same typed actions as the GUI, with permission checks, logs and undo.
- **Models are pluggable.** Local weights, containers, cloud APIs and remote nodes all look the same to the system. You choose, and you can switch without losing your work.
- **Built on a real Linux base.** An immutable Fedora bootc foundation with a Linux 6.19 kernel, so every normal Linux app still runs.

<p align="center"><img src="https://raw.githubusercontent.com/sorabbyngo-os/.github/main/assets/divider.svg" alt="" width="100%"></p>

## How the pieces fit

```text
      You  ──  speak · type · touch
                         │
                         ▼
 ┌──────────────────────────────────────────────┐
 │  Vanta       the spatial Wayland desktop     │
 │   └─ Chameha   voice and personality         │
 └───────────────────────┬──────────────────────┘
                         ▼
 ┌──────────────────────────────────────────────┐
 │  AION        plans, routes and mediates      │
 │   └─ CML       safety, alignment, privacy    │
 └───────────────────────┬──────────────────────┘
                         ▼
 ┌──────────────────────────────────────────────┐
 │  ObjectSpace   objects and spaces (the world)│
 └───────────────────────┬──────────────────────┘
                         ▼
 ┌──────────────────────────────────────────────┐
 │  Byngonet · Sentinel · HAL · Fedora base     │
 │  mesh network · security · hardware · image  │
 └──────────────────────────────────────────────┘
```

> **ObjectSpace** defines the world. **AION** decides and mediates. **Vanta** is how you see and touch it. **Chameha** is how you speak with it.

<p align="center"><img src="https://raw.githubusercontent.com/sorabbyngo-os/.github/main/assets/divider.svg" alt="" width="100%"></p>

## The repositories

### Experience

| Repository | What it is |
| --- | --- |
| [**vanta**](https://github.com/sorabbyngo-os/vanta) | The AI-native spatial desktop: a Wayland compositor in Rust on Smithay. |
| [**chameha**](https://github.com/sorabbyngo-os/chameha) | The voice and personality of the OS, living inside Vanta. |
| [**ai-terminal**](https://github.com/sorabbyngo-os/ai-terminal) | The terminal with AI assistance built in. |

### Intelligence

| Repository | What it is |
| --- | --- |
| [**aion**](https://github.com/sorabbyngo-os/aion) | The AI runtime and control plane that turns intent into safe, observable action. |
| [**objectspace**](https://github.com/sorabbyngo-os/objectspace) | The spatial object runtime: the world model that Vanta renders. |
| [**cml**](https://github.com/sorabbyngo-os/cml) | The Cognitive Mediation Layer: safety, alignment and privacy enforcement. |
| [**cognitive-runtime**](https://github.com/sorabbyngo-os/cognitive-runtime) | The earlier cognitive runtime, kept as the historical precursor to AION. |
| [**ai-sandbox**](https://github.com/sorabbyngo-os/ai-sandbox) | An isolated environment for running models and agents with least privilege. |
| [**byngox**](https://github.com/sorabbyngo-os/byngox) | The original 8-agent swarm engine over NATS. Superseded: models are now pluggable backends. |

### Network

| Repository | What it is |
| --- | --- |
| [**byngonet**](https://github.com/sorabbyngo-os/byngonet) | An AI-native mesh network protocol with swarm routing and post-quantum security. |
| [**dmz**](https://github.com/sorabbyngo-os/dmz) | A one-way wall between the private core and the public platform. |

### Security and trust

| Repository | What it is |
| --- | --- |
| [**sentinel**](https://github.com/sorabbyngo-os/sentinel) | The autonomous security, trust and threat-intelligence engine. |
| [**sentinel-runtime**](https://github.com/sorabbyngo-os/sentinel-runtime) | The runtime that executes Sentinel's policies on a live system. |
| [**sorabbyngo-security**](https://github.com/sorabbyngo-os/sorabbyngo-security) | System-wide security configuration and hardening. |
| [**sorabbyngo-cyberwall**](https://github.com/sorabbyngo-os/sorabbyngo-cyberwall) | The network and application firewall layer. |
| [**capd**](https://github.com/sorabbyngo-os/capd) | The capability daemon: fine-grained permissions for what each component may do. |
| [**domain-mode**](https://github.com/sorabbyngo-os/domain-mode) | Domain-based isolation modes for separating workloads. |

### System and resilience

| Repository | What it is |
| --- | --- |
| [**sorabbyngo-os**](https://github.com/sorabbyngo-os/sorabbyngo-os) | The OS umbrella: Linux 6.19.10 kernel, HAL and AI runtime, with NodeID and Byngonet modules. |
| [**sorabbyngo-kernel**](https://github.com/sorabbyngo-os/sorabbyngo-kernel) | The kernel tree. |
| [**sorabbyngo-patches**](https://github.com/sorabbyngo-os/sorabbyngo-patches) | The patch set on Linux 6.19.10, including the NodeID and Byngonet drivers. |
| [**fedora-base**](https://github.com/sorabbyngo-os/fedora-base) | The Fedora-derived base, image definitions and inherited system components. |
| [**hal**](https://github.com/sorabbyngo-os/hal) | The hardware abstraction layer, including sensors. |
| [**hypervisor-engine**](https://github.com/sorabbyngo-os/hypervisor-engine) | Virtualization support for isolated workloads. |
| [**sorabbyngofs**](https://github.com/sorabbyngo-os/sorabbyngofs) | The AI-native virtual filesystem module. |
| [**byngo-press**](https://github.com/sorabbyngo-os/byngo-press) | The compression layer. |
| [**resource-governor**](https://github.com/sorabbyngo-os/resource-governor) | CPU, memory and I/O limits so no component starves the others. |
| [**os-watchdog**](https://github.com/sorabbyngo-os/os-watchdog) | Watches system health and restarts what fails. |
| [**self-healing**](https://github.com/sorabbyngo-os/self-healing) | Automatic detection and repair of faults. |
| [**omega**](https://github.com/sorabbyngo-os/omega) | Core system orchestration. |
| [**sorabbyngo-superdevice**](https://github.com/sorabbyngo-os/sorabbyngo-superdevice) | Device support and multi-device continuity. |

<p align="center"><img src="https://raw.githubusercontent.com/sorabbyngo-os/.github/main/assets/divider.svg" alt="" width="100%"></p>

## Where to start

| If you want to... | Start with |
| --- | --- |
| See what the desktop will feel like | [**vanta**](https://github.com/sorabbyngo-os/vanta) |
| Understand how AI acts on the system safely | [**aion**](https://github.com/sorabbyngo-os/aion) |
| Understand the OS image and base | [**fedora-base**](https://github.com/sorabbyngo-os/fedora-base) |
| Look at the network and security design | [**byngonet**](https://github.com/sorabbyngo-os/byngonet) and [**sentinel**](https://github.com/sorabbyngo-os/sentinel) |

Most repositories are **pre-alpha**. The architecture is settled, the code is catching up, and each README states its own status honestly.

## Contributing

Ideas, issues and pull requests are welcome. Please open an issue to discuss anything large before you write it, and read the principles in [**vanta**](https://github.com/sorabbyngo-os/vanta/blob/main/README.md#rules-that-do-not-bend), since they apply across the whole system.

Each repository carries its own license in its `LICENSE` file. Check it before you reuse code.

<p align="center"><img src="https://raw.githubusercontent.com/sorabbyngo-os/.github/main/assets/divider.svg" alt="" width="100%"></p>

<p align="center">
  <b>Sorabbyngo</b> · <i>The Rhythm of Digital Life</i><br>
  Built for everyone.
</p>
