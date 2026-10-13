Sorabbyngo OS

**The Rhythm of Digital Life**

> What if the operating system were not a place you visit —  
> but a presence that works with you?

Sorabbyngo OS is an independent, AI-native Linux system.  
It keeps the power, scripts, and compatibility of Linux —  
and rebuilds the *experience* around intent, space, and continuity.

Not a desktop with a chatbot bolted on.  
Not a cloud appliance that dies offline.  
A real OS: bootable, inspectable, local-first —  
with intelligence as a **runtime**, not a product pitch.

---

## The shift

Computing is still organized like a warehouse:

```text
User → Application → File → Kernel
Sorabbyngo organizes it like a workshop you can talk to:
User → Intent or Direct action
         ↓
       Vanta          (spatial desktop — what you see and touch)
         ↓
       AION           (AI runtime — plans, routes, mediates)
         ↓
       ObjectSpace    (objects, spaces, relationships)
         ↓
       Linux          (files, processes, hardware — still real)
Old center
Sorabbyngo center
Applications
Spaces
Files
Objects
Assistant app
AION (control plane)
Manual SSH / IP
Byngonet continuity
AI as feature
AI as mediated runtime
Applications remain. Files remain.
They become implementation details under a model built for work that continues.
Ambition
Inspired by the idea of an OS you can speak with — continuous across devices, present without being invasive — Sorabbyngo aims at:
A companion environment — Chameha as voice and personality inside the desktop, from install through daily use
A spatial desktop — Vanta: Wayland, tiling and freedom, motion that communicates, not decorates
A safe intelligence layer — AION: models are backends; the system owns the path from intent to effect
A world model — ObjectSpace: projects, documents, tools, and sessions as structured objects
Multi-device presence — Byngonet: continue a thought on another machine without ceremony
An independent Linux distribution — Fedora bootc / ostree lineage for atomic updates and rollbacks; our identity above it
The bar is high. The discipline is to build the center first: Vanta + AION + ObjectSpace on a solid immutable base.
Architecture
┌──────────────────────────────────────────────────────────┐
│                     User                                 │
│            voice · touch · keyboard · gesture            │
└─────────────────────────┬────────────────────────────────┘
                          │
┌─────────────────────────▼────────────────────────────────┐
│  VANTA — spatial Wayland environment                     │
│  compositor · shell · settings · intent client           │
│  Chameha lives here (conversation & personality)         │
└─────────────────────────┬────────────────────────────────┘
                          │ typed actions / intent
┌─────────────────────────▼────────────────────────────────┐
│  AION — AI runtime & control plane                       │
│  backend selection · context assembly · tool mediation   │
│  local models · user API keys · remote nodes             │
└───────────────┬─────────────────────┬────────────────────┘
                │                     │
                ▼                     ▼
        ObjectSpace              Byngonet
     objects · spaces         inter-node mesh
     relationships            discovery · handoff
                │
                ▼
┌───────────────────────────────────────────────────────────┐
│  Linux substrate (Fedora bootc lineage)                   │
│  ostree/bootc · RPM · systemd · SELinux · kernel          │
│  “everything is a file” remains true underneath           │
└───────────────────────────────────────────────────────────┘
Component
Role
Vanta
Spatial desktop — Smithay/Wayland compositor + shell
Chameha
Voice, personality, dialogue (inside Vanta)
AION
AI runtime — not a model; the mediation layer
ObjectSpace
Intelligent objects and spaces
Byngonet
Secure communication between Sorabbyngo nodes
Sentinel
Health, supervision, recovery
fedora-base
Immutable base, image recipes, inherited stack
Technical foundations
Layer
Choice
Rationale
Base OS
Fedora bootc / ostree
Atomic updates, rollbacks, container-native images
Packages
RPM
Matches Fedora/RHEL ecosystem; proven tooling
Init
systemd
Sessions, cgroups, service supervision (with Sentinel above)
MAC
SELinux
Confine AI backends and privileged paths
Desktop
Wayland + Smithay (Rust)
Modern display stack; Vanta owns the session
AI integration
AION as control plane
Pluggable local / API / remote backends
Isolation
cgroups, containers (Podman), least privilege
Models propose; AION mediates; no raw root for models
Architecture (first)
x86_64
Intel/AMD first; NVIDIA optional via RPM Fusion patterns
Kernel: track the Fedora release pinned by the bootc base image — not a random mainline fork — until real out-of-tree patches demand otherwise.
Philosophy under the hood: Linux remains Linux.
Everything is a file at the substrate.
Objects and spaces are the native language above it.
Design principles
Direct path always works — unplug AI; the machine remains a complete desktop.
Compositor never waits on a model — frames first; intelligence is asynchronous.
One door for action — GUI, shortcuts, and AION share one mediated API.
Local-first — core experience survives without the cloud.
You choose the intelligence — models are backends; better ones appear monthly.
Predictable and undoable — power without mystery.
Presence across distance — multi-device continuity is a product capability, not a manual ritual.
Open core, honest boundaries — system runnable offline; optional services may fund the project later without locking the foundation.
Status
Pre-alpha. Active design and foundation work.
Track
State
Vision & component boundaries
Defined
Fedora bootc inheritance (fedora-base)
Sources and image recipes in prep
Vanta (spatial desktop)
Design + Phase 0 scaffolding
AION
Runtime architecture defined; implementation ahead
ObjectSpace / Byngonet / Sentinel
Spec and early research
Earlier experiments (custom agents, embedded planners, broad repo sprawl) informed the present shape: fewer cores, clearer contracts, ship the center.
Repository map
Repository
Purpose
sorabbyngo-os (this)
Product face, vision, orchestration
vanta
Spatial desktop environment
aion
AI runtime and control plane
objectspace
Spatial object runtime
chameha
Voice and personality
byngonet
Inter-node communication
fedora-base
Immutable base and build inheritance
sentinel
Monitoring and self-healing
Open direction
The core system is intended to be open and independently runnable.
Sustainable paths (later, after something real ships):
optional hosted intelligence and multi-device relays
professional support and fleet features
hardware or vertical bundles
First the rhythm must be real.
Then the economy can follow.
License
To be decided.
All rights reserved until a license is published.
Sorabbyngo
The Rhythm of Digital Life
Not merely a system you operate —
a presence that works with you.
