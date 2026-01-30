# UAE AI/Dev Ops Tech Setup (Mac mini M4 + Windows 11 + Remote Access)

This repository documents and manages a real-world deployment for a UAE-based digital / AI team.

We currently work on Windows 11 laptops (16GB RAM, SSD) with ~25 Mbps wireless internet.
We are standardizing on **Mac mini (M4)** as a **central compute node** for stable development and AI workflows, accessed locally (desk setup) and remotely (AnyDesk), while keeping Windows laptops as primary “client” devices.

---

## The problem (today)
- Wireless internet (~25 Mbps) causes inconsistent remote access performance (lag, blur, drops).
- No standardized monitors, keyboards, mice, docking layout, or shared storage.
- Tool setup is inconsistent across team machines (Claude Code, cloud IDEs, automation workflows).
- No single source of truth for procurement, cost tracking, security posture, or rollout steps.

---

## The vision (target state)
A stable, high-performance environment where:
- Mac mini M4 machines provide consistent compute for dev + AI tooling.
- Windows laptops connect reliably to Mac minis for coding, builds, automations, and workflows.
- Files are stored in a controlled shared storage layer (NAS or cloud) with proper backup.
- Internet is upgraded to wired fiber and the internal network is designed for low latency.
- Hardware and software are standardized so onboarding is fast and predictable.
- Costs and decisions are tracked like an operations project, not an ad-hoc setup.

---

## Why Mac mini + remote access?
Mac minis are compact, power-efficient “always-on” machines that can serve as a dedicated dev/AI node.
They are ideal as:
- a stable build box,
- a consistent environment for tools (Claude Code, automation runners, dockerized services),
- a team-shared compute layer.

Mac mini M4 configurations and ports/specs are documented in `hardware/mac-mini-m4.md`. :contentReference[oaicite:1]{index=1}

Remote access is a practical bridge:
- Team stays on Windows 11 laptops
- Mac mini becomes the “compute core”
- Developers connect via AnyDesk / similar tools when local access isn’t possible

---

## Why internet + infrastructure matters (UAE reality)
Remote access quality depends on:
- **upload speed**, latency, jitter (not just download speed),
- wired vs wireless stability,
- router quality and internal network design.

Today we’re on ~25 Mbps wireless. That can be “okay” for browsing but unreliable for:
- remote desktop at high resolution,
- cloud IDE streaming,
- multi-monitor workflows,
- large repo pulls, container builds, and artifact uploads.

UAE home/SMB internet plans and availability differ by location and building provider, so Phase 1 focuses on selecting a wired fiber plan and ensuring correct installation and internal wiring. (See `rollout/phase-1-internet.md`) :contentReference[oaicite:2]{index=2}

---

## What success looks like
**Operational success**
- Remote session is stable for 2–4 hours with minimal lag.
- Team can onboard a new developer in < 60 minutes (accounts + tools + repo access).
- Builds and automation jobs run consistently with logging + backups.

**Engineering success**
- Standard dev workflow and repo structure is documented and enforced.
- Shared storage is reliable and backed up.
- Security baseline is in place (accounts, access, encryption, updates).

**Business success**
- Procurement is tracked with clear costs (CapEx + OpEx).
- Rollout is phased, measurable, and scalable (1 workstation → multiple).

---

## How to use this repo
Start here:
1. `docs/01_current-setup.md`
2. `docs/02_target-setup.md`
3. `rollout/phase-1-internet.md` (critical path)
4. `costs/procurement-plan.md`

This repo is designed to become the **brain of the operation**:
- decisions
- costs
- standards
- workflows
- risks
- rollout status

---

## Quick links
- Current setup: `docs/01_current-setup.md`
- Target setup: `docs/02_target-setup.md`
- Risks: `docs/03_risks-and-mitigations.md`
- Hardware: `/hardware`
- Costs: `/costs`
- Rollout: `/rollout`
- Workflows: `/workflows`
