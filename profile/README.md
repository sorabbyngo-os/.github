<div align="center">

<img src="https://raw.githubusercontent.com/sorabbyngo-os/.github/main/assets/sorabbyngo-os-logo.jpeg" alt="Sorabbyngo OS" width="340"/>

<br/>

# Sorabbyngo OS

### The Operating System That Thinks.

<br/>

*Africa's first AI-native sovereign operating system — built from the ground up.*

<br/>

[![Kernel](https://img.shields.io/badge/Kernel-Linux%206.19.10--sorabbyngo-88ff44?style=for-the-badge&labelColor=040a04)](https://github.com/sorabbyngo-os)
[![Status](https://img.shields.io/badge/Status-Active%20Development-FF6B35?style=for-the-badge)](https://github.com/sorabbyngo-os)
[![Division](https://img.shields.io/badge/Division-Sorabbyngo-6C3FC4?style=for-the-badge)](https://github.com/sorabbyngo-headquarters)

</div>

---

<br/>
sorabbyngo init
loading kernel 6.19.10-sorabbyngo...
initializing NodeID driver...
initializing Byngonet driver...
AI core: ONLINE
Chameha interface: LOADED
CML safety layer: ACTIVE
system services: ONLINE
user environment: LOADED


Sorabbyngo OS
System Ready.
_
<br/>

---

<br/>

## What is Sorabbyngo OS?

Sorabbyngo OS is Africa's sovereign, AI-native operating system — built on Linux 6.19.10 with two proprietary kernel modules, a custom AI runtime, and an offline-first architecture designed for the most demanding and resource-constrained environments on earth.

It is not a Linux distribution. It is not a fork. It is a complete sovereign OS platform — from the kernel to the interface — built to run every device in the Sorabbyngo ecosystem.

<br/>

---

<br/>

## Core Architecture

<div align="center">

| Layer | Component | Role |
|---|---|---|
| 🧠 **AI Runtime** | Byngox | 8-agent AI swarm engine running on-device |
| 🌐 **Network** | Byngonet | AI-native mesh protocol, post-quantum crypto |
| 🆔 **Identity** | NodeID | Hardware-bound cryptographic device fingerprint |
| 🎙️ **Interface** | Chameha | Voice-first AI personality layer, bilingual |
| 🛡️ **Safety** | CML | Cognitive Mediation Layer — AI safety & compliance |
| ⚙️ **Kernel** | Linux 6.19.10-sorabbyngo | Custom kernel with proprietary drivers |
| 📦 **Init** | BusyBox + Buildroot 2024.02 | Lightweight, no systemd dependency |


# Sorabbyngo OS Ecosystem Status

**Engineering Architecture Update — June 2026**

---

# Purpose

This document defines the current architecture of the Sorabbyngo ecosystem after the latest engineering decisions. It is intended to guide all contributors and keep every repository aligned as development scales.

---

# High-Level Architecture

```
                     USER
          Voice • Touch • Keyboard
                    │
                    ▼
               CHAMEHA
      Personality • Conversation
      Intent • AION Runtime
                    │
                    ▼
               BYNGOX
     Multi-Agent Cognitive Engine
                    │
                    ▼
        Capability & Hardware APIs
                    │
        ┌───────────┴────────────┐
        │                        │
        ▼                        ▼
Hardware Agent             Byngonet
(Device Knowledge)       Networking Layer
        │                        │
        └───────────┬────────────┘
                    ▼
          Sorabbyngo Base
     Immutable Fedora Foundation
                    │
                    ▼
               Linux Kernel
                    │
                    ▼
                Hardware
```

---

# Repository Responsibilities

## Chameha

Repository:

```
sorabbyngo-os/chameha
```

Purpose:

Chameha is the user-facing AI.

It is responsible for:

* Voice interaction
* Chat interaction
* Personality
* Long-term conversations
* Intent understanding
* User preferences
* Memory access
* Running the AION runtime
* Request orchestration

Users never interact directly with Byngox.

To the user there is only **Chameha**.

---

## AION

AION is **not a standalone repository.**

AION lives inside Chameha.

Responsibilities:

* Device orchestration
* Intent execution
* Hardware control
* Capability planning
* Safe execution
* Scheduling
* Action verification

AION converts:

```
User Intent
      ↓
Execution Plan
      ↓
Byngox
      ↓
Operating System
```

---

## Byngox

Repository:

```
sorabbyngo-os/byngox
```

Purpose:

Distributed reasoning engine.

Byngox never communicates with users.

Responsibilities:

* Multi-agent reasoning
* Planning
* Context analysis
* Medical reasoning
* Learning
* Security reasoning
* Risk evaluation
* Decision aggregation

Current architecture:

```
Coordination Agent

├── Health
├── Drug
├── Learning
├── Population
├── Security
├── Context
├── Network
├── Hardware
```

The new **Hardware Agent** becomes a first-class agent.

---

## Hardware Agent

New agent inside Byngox.

Purpose:

Maintain complete awareness of the current device.

It continuously understands:

CPU

GPU

RAM

Battery

Thermals

Storage

Network

Sensors

Camera

Microphone

Power source

Display

Accelerators

Running workloads

Resource limits

Hardware health

Example:

```
User:

Train this model.

↓

Hardware Agent

RTX 3050
8 GB RAM

↓

Byngox

Chooses quantized model

↓

AION executes safely.
```

Another example:

```
User:

Render a 4K video.

↓

Hardware Agent

Battery = 5%

↓

Reject or delay operation.
```

This prevents the AI from damaging the device or making unrealistic decisions.

---

## Byngonet

Repository:

```
sorabbyngo-os/byngonet
```

Updated mission:

Byngonet is **NOT an AI.**

AI responsibilities have moved into Byngox.

Byngonet becomes the networking backbone.

Responsibilities:

* Device discovery
* Mesh networking
* Offline synchronization
* Node identity
* Secure communication
* Peer routing
* Remote execution transport
* Network health
* Presence
* Service discovery
* File synchronization
* Session transport
* Multi-device communication

Think of it as:

```
AI decides

↓

Byngonet transports
```

Not

```
Byngonet thinks.
```

---

## Sorabbyngo Base

Repository:

```
sorabbyngo-base-kernel/sorabbyngo-base
```

Purpose:

Operating system foundation.

Contains:

* Fedora Silverblue
* bootc
* rpm-ostree
* Kernel patches
* Security
* Runtime
* APIs
* Core services

No AI logic belongs here.

It only exposes capabilities.

---

# Remote Device Control

Remote execution now follows this chain.

```
User

↓

Chameha

↓

AION

↓

Capability Broker

↓

Byngonet

↓

Target Device

↓

Hardware APIs

↓

Result

↓

Back to User
```

The user never configures SSH.

No command lines.

No terminal access.

Everything is capability-based.

---

# Capability Model

Applications never receive unrestricted hardware access.

Instead:

```
Application

↓

Capability Broker

↓

Permission Engine

↓

Hardware API

↓

Hardware
```

Every action is:

* authenticated
* authorized
* audited
* revocable

---

# Current Engineering Principles

1. Chameha is the only user-facing AI.

2. AION lives inside Chameha.

3. Byngox performs reasoning only.

4. Hardware knowledge belongs to the Hardware Agent.

5. Byngonet handles networking only.

6. Sorabbyngo Base contains no AI.

7. Every hardware action passes through the Capability Broker.

8. Remote device control is capability-based, not SSH-based.

9. AI decisions are always constrained by actual device capabilities.

10. Desktop and Mobile are the first supported platforms.

---

# Current Repository Status

```
sorabbyngo-base
        │
        ├── Fedora Silverblue
        ├── bootc
        ├── Security
        ├── Runtime
        ├── APIs
        └── Core Services

                ▲

        Byngonet
(Network & Connectivity)

                ▲

        Hardware Agent
(Device Awareness)

                ▲

            Byngox
(Reasoning Engine)

                ▲

      Chameha + AION
(User Experience)

                ▲

              User
```

---

# Development Priority

Current roadmap:

**Phase 1**

* Sorabbyngo Base
* Core services
* Capability Broker
* Permission Engine

**Phase 2**

* Hardware Agent
* Byngonet transport
* Device APIs

**Phase 3**

* AION integration
* Remote control
* Automation

**Phase 4**

* Sorabbyngo Mobile

**Phase 5**

* Sorabbyngo Desktop

This document supersedes earlier designs where networking intelligence resided inside Byngonet. Intelligence is now centralized in Byngox, while networking, transport, and synchronization remain the responsibility of Byngonet.



</div>

<br/>

---

<br/>

## What Makes It Different

> Most operating systems were built for the West — stable power, fast internet, expensive hardware. Sorabbyngo OS was built for Africa.

- 🔒 **Sovereign** — no foreign dependencies, no foreign telemetry, no foreign cloud
- 📡 **Offline-first** — full AI and system capability with zero internet connectivity
- 🆔 **Hardware identity** — every device cryptographically identified via NodeID
- 🌍 **Africa-native** — designed for low connectivity, distributed nodes, adversarial environments
- 🧠 **AI at the kernel level** — intelligence baked into the OS, not bolted on top
- ⚡ **Lightweight** — BusyBox init, no systemd, optimised for constrained hardware

<br/>

---

<br/>

## Proprietary Kernel Modules

### NodeID
Hardware-bound cryptographic device identity. Every device running Sorabbyngo OS gets a unique, tamper-proof identity tied to its hardware — enabling secure authentication, audit trails, and network identity without relying on external certificate authorities.

### Byngonet
Netfilter-based network identity and packet tagging. An AI-native mesh network protocol with post-quantum cryptography — enabling offline-first distributed networking, swarm routing, and sovereign communications between Sorabbyngo devices.

<br/>

---

<br/>

## Devices It Runs On

| Device Class | Status |
|---|---|
| Desktop / Laptop | ✅ Active |
| Embedded IoT | ✅ Active |
| Edge servers | ✅ Active |
| Smartphones | 🔜 Planned |
| Drones & Robotics | 🔜 Planned |
| Satellite terminals | 🔜 Planned |
| Autonomous vehicles | 🔜 Planned |

<br/>

---

<br/>

## Repositories

| Repo | Description |
|---|---|
| [**sorabbyngo-os**](https://github.com/sorabbyngo-os/sorabbyngo-os) | Core OS — kernel, HAL, AI runtime |
| [**sorabbyngo-patches**](https://github.com/sorabbyngo-os/sorabbyngo-patches) | Kernel patch set — NodeID + Byngonet on Linux 6.19.10 |
| [**byngonet**](https://github.com/sorabbyngo-os/byngonet) | AI-native mesh network driver |
| [**chameha**](https://github.com/sorabbyngo-os/chameha) | AI personality and voice interface layer |
| [**cml**](https://github.com/sorabbyngo-os/cml) | Cognitive Mediation Layer — safety and compliance |
| [**byngox**](https://github.com/sorabbyngo-os/byngox) | 8-agent AI swarm inference engine |
| [**sorabbyngo-build**](https://github.com/sorabbyngo-os/sorabbyngo-build) | Architecture decisions, phase plans, engineering roadmap |

<br/>

---

<br/>

## Build Info
Kernel        Linux 6.19.10-sorabbyngo
Compiler      GCC 12
Drivers       NodeID · Byngonet
Init          BusyBox · Buildroot 2024.02
Target        x86_64 · ARM (planned)
Boot          QEMU verified · hardware boot in progress
AI Runtime    Byngox (on-device inference)
Interface     Chameha (voice-first, offline)
Safety        CML middleware

<br/>

---

<br/>

## Part of Sorabbyngo

| Component | Role |
|---|---|
| [**Soraxis**](https://github.com/soraxis-tech) | Hardware that runs Sorabbyngo OS |
| [**Sorabyte**](https://github.com/sorabyte-cloud) | AI compute and cloud layer |
| [**Citadel**](https://github.com/citadel-sec) | Security hardening and compliance |
| [**Novela**](https://github.com/novela-health) | Health platform running on Sorabbyngo OS |
| [**Vector**](https://github.com/sorabbyngo-vector) | Logistics fleet running Sorabbyngo OS |

<br/>

---

<br/>

<div align="center">

**Sorabbyngo OS** is built by [Sorabbyngo Company](https://github.com/sorabbyngo-headquarters)
<br/>
Kisii, Kenya · 2026
<br/><br/>
*Rhythm of Digital Life*

</div>
