<!-- readme-standard: 2026-11-02 -->
<div align="center">

<img src="assets/banner.svg" width="100%" alt="Littlebird Ambassador: a sun held by an open circle with waves drawing in beneath it, one morning brief at a time.">

# Littlebird Ambassador 🐦

*Context engine for the agent fleet: always-on observation, one morning brief at a time.*

[![License: MIT](https://img.shields.io/badge/license-MIT-1a1a2e?style=flat-square)](LICENSE)
[![Public Preview](https://img.shields.io/badge/%F0%9F%8C%90%20Public%20Preview-Available-5c1a2b?style=flat-square)](https://drasticstatic.github.io/littlebird-ambassador-public-preview/)
[![Synced via GitHub Actions](https://img.shields.io/badge/Synced%20via-GitHub%20Actions-1a1a2e?style=flat-square)](https://github.com/drasticstatic/littlebird-ambassador/actions/workflows/sync-public.yml)
[![Built with Claude Code](https://img.shields.io/badge/Built%20with-Claude%20Code%20CLI-5c1a2b?style=flat-square)](https://code.claude.com/docs/en/overview)
[![Status](https://img.shields.io/badge/Status-%F0%9F%94%A5%20Active%20Build-800020?style=flat-square)](https://github.com/drasticstatic/littlebird-ambassador)

<img src="assets/icons/map-pin.svg" width="16" height="16" alt=""> **You are here:** drasticstatic lab › source `littlebird-ambassador` (private) → twin `littlebird-ambassador-public-preview` (public) · `main` is the working branch

</div>

## <img src="assets/icons/compass.svg" width="24" height="24" alt=""> TL;DR

1. <img src="assets/icons/bird.svg" width="16" height="16" alt=""> **What this is.** How Littlebird's always-on context layer feeds into Christopher Wilson's agent fleet, and is eventually fed by it: the planning here, a sanitized showcase on the public preview.
2. <img src="assets/icons/users-round.svg" width="16" height="16" alt=""> **Who it is for.** Anyone curious what a context layer does for a whole fleet of agents, not just one assistant.
3. <img src="assets/icons/footprints.svg" width="16" height="16" alt=""> **Do this first.** [Explore the public preview](https://drasticstatic.github.io/littlebird-ambassador-public-preview/).

---

<img src="assets/icons/globe.svg" width="16" height="16" alt=""> **[Explore the Public Preview →](https://drasticstatic.github.io/littlebird-ambassador-public-preview/)**

---

> <img src="assets/icons/lock.svg" width="16" height="16" alt=""> **Public mirror notice:** This repository is partially mirrored to a public preview via an automated GitHub Actions pipeline. The public version includes only sanitized, generalized content. Private planning notes, program specifics, and personal context are excluded.

---

## <img src="assets/icons/list-checks.svg" width="24" height="24" alt=""> Table of Contents

- [What This Is](#what-this-is)
- [The Goal](#the-goal)
- [Capabilities](#capabilities)
- [Architecture](#architecture)
- [Collaboration](#collaboration)
- [Suggest a change](#suggest-a-change)
- [License](#license)

---

<a id="what-this-is"></a>
## <img src="assets/icons/bird.svg" width="24" height="24" alt=""> What This Is

Littlebird is a context engine that runs continuously in the background, building a picture of how Christopher Wilson works — across an AI agent fleet spanning Claude Code CLI and Augment Intent, not just a single tool. This repo tracks that integration: how Littlebird's context layer feeds into, and is eventually fed by, the rest of the ecosystem.

**Developer / builder:** Christopher Wilson (`drasticstatic`)
**AI agents:** Alfred (Claude Code CLI) — public-preview lane & showcase content

---

<a id="the-goal"></a>
## <img src="assets/icons/sun.svg" width="24" height="24" alt=""> The Goal

Turn always-on context capture into something the agent fleet can actually use — daily briefings that carry forward into agent sessions, and eventually a two-way feed where the fleet's own work informs what Littlebird understands. The public-preview lane exists to show how this fits together, without exposing the private context data behind it.

- **Daily context handoff** — a standing morning routine summarizes what matters and hands it to whichever agent picks up the day's work
- **Full-screen observation** — Littlebird watches both Claude Code CLI and Augment Intent sessions, not just one tool in isolation
- **Cross-agent showcase** — demonstrating how a context layer like this strengthens an entire agent fleet, not just a single assistant

---

<a id="capabilities"></a>
## <img src="assets/icons/sparkles.svg" width="24" height="24" alt=""> Capabilities

### <img src="assets/icons/eye.svg" width="20" height="20" alt=""> Core

- Continuous, consented screen observation across the agent fleet's working environment
- A daily briefing routine, tuned over time as calibration improves
- Cross-referencing agent-fleet documentation to keep Littlebird's own understanding current

### <img src="assets/icons/wrench.svg" width="20" height="20" alt=""> Technical

- Public-preview lane synced via the same GitHub Actions pipeline used across this ecosystem
- Cross-references into `trading-assistant` (Fortuna's domain) and `mystarch_chief-of-staff` (Augment Intent's coordination seat) as showcase content develops

---

<a id="architecture"></a>
## <img src="assets/icons/layers.svg" width="24" height="24" alt=""> Architecture

- **Private repo (this one):** planning notes, calibration status, and integration decisions
- **Public preview:** sanitized showcase content — no personal calendar, program, or account details
- **Sync:** GitHub Actions, allowlist model — everything private by default, only explicitly-classified paths reach the public mirror

```mermaid
flowchart LR
  P[Private repo<br/>planning and decisions] --> A{{Allowlist:<br/>named paths only}}
  A --> T{{Tripwire reads<br/>every file}}
  T -->|clean| M[Public preview<br/>sanitized showcase]
  T -->|refused| S[Nothing is published]
```

---

<a id="collaboration"></a>
## <img src="assets/icons/handshake.svg" width="24" height="24" alt=""> Collaboration

This is a solo-developer project (Christopher Wilson) built with AI-agent assistance. Issues and discussion on the public preview are welcome; the private planning content in this repo stays private.

---

<a id="suggest-a-change"></a>
## <img src="assets/icons/git-pull-request.svg" width="24" height="24" alt=""> Suggest a change

Noticed something? Open an [issue](../../issues) or a pull request against `main`; Christopher reads them and a person with the role merges. Not on GitHub? Reach him through any channel on [his profile](https://github.com/drasticstatic). On the public preview, please open an issue rather than a pull request: its files are synced from the private source, so a change made only there would be overwritten.

---

<a id="license"></a>
## <img src="assets/icons/scroll-text.svg" width="24" height="24" alt=""> License

[MIT](LICENSE) — applies to this repo's own content (docs, configuration, showcase code). It does not extend to Littlebird's own product, brand, or any third-party service referenced here.

---

*Built and maintained by [drasticstatic](https://github.com/drasticstatic) · w/ Anthropic's Claude Code CLI*

<sub>The front door follows the living [README standard](https://github.com/drasticstatic/my-template/blob/main/README-STANDARD.md). Copy it, improve it. Icons: Phosphor duotone (MIT).</sub>
