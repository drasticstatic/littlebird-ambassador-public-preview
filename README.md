# Littlebird Ambassador — Planning & Context

Private planning repo for Christopher Wilson's Littlebird **Founding Ambassador** opportunity. This is a context-preservation and planning artifact, not an integration — no agent in this ecosystem can sign up for the program, accept payment, or operate Littlebird's screen recording on Christopher's behalf. It exists so the plan survives independent of any one chat session, ready for Alfred to build a public-preview lane from in a future session.

## The opportunity

Littlebird's Brand Ambassador program: [littlebird.ai/brand-ambassadors](https://littlebird.ai/brand-ambassadors)

Christopher received a "Founding Ambassador" invite — paid, and specifically for people who are already active, high-signal Littlebird users with stories worth sharing. The invite email opened with:

> "Dear Littlebird Expert - We want you to become our Founding Ambassador and get paid; You're getting this because you're one of the most active people on Littlebird."

## Current Littlebird relationship (as of this writing)

- **Free tier only.** Christopher hasn't yet upgraded to a paid tier.
- **24/7 consented screen recording** has been running throughout — Littlebird's context engine has been building a picture of Christopher and his work the whole time, even on the free tier.
- **One configured routine: "Morning Brief"** — a daily 7am routine, live and successfully producing output since **May 30, 2026**. This is the one piece of Littlebird's output Christopher currently has a habit of using.
- **Calibration still pending.** Christopher hasn't yet had a dedicated conversation with Littlebird to correct inaccuracies in what it currently believes about him — he's been "too busy talking to Fortuna" to make time for it. The plan is to eventually feed Littlebird corrective markdown files (from this ecosystem's own docs) to speed that calibration up once he does sit down with it.

### The Morning Brief prompt (verbatim)

This is the exact routine prompt Christopher runs each morning:

> Give me my morning brief. What's on today — top priorities, meetings I should prep for, and anything I'm at risk of dropping or letting slip through the cracks. Keep it to what I'd actually want to read before I get started.
>
> In addition to the primary cwilson.cswproductions@gmail.com calendar, check ALL calendars across drasticstatic@gmail.com — not just the primary — when summarizing today's schedule; include events from all subscribed calendars: {Google-drasticstatic, Google-Family, Apple-drasticstatic, Apple-Family, Trading, Trading | Inevitrade, web3 | blockchain, Recovery, PIR: zoom.main.pir, & PIR: Service Mtg}
>
> Also include a summary of the previous day's futures trading observations (and anything related that can help me give Claude/Fortuna all the context that may slip through the cracks as everything ultimately affects my trading) until ideally we can afford to pay for Littlebird and create a tailored end-of-session trading journaling routine :-)
>
> Also add a concluding TL;DR version summary of what was completed in the previous 24 hours in a sharable journal-like format for AI agents and/or humans to be able to reference. Then followed by a little more detail for further context that I can pass to other agents :-)

Two things worth noting about this prompt as written:
1. It already spans **9 calendars across 2 Google accounts and 2 Apple accounts** — Christopher's whole life, not just trading.
2. It's explicitly designed for **AI-agent handoff** — the TL;DR + detail structure exists so this output can be pasted straight into a session with Fortuna, Alfred, or any other agent in the fleet, not just read by a human.

## The plan, as currently understood

1. **Calibration conversation with Littlebird** — Christopher needs to sit down and correct what Littlebird currently has wrong about him. He may hand it markdown files from this ecosystem (trading-assistant, divorce-custody-assistant, etc.) to accelerate that.
2. **First cross-agent showcase use case: trading data.** Once Fortuna has digested Christopher's full trading backlog (in progress as of this writing — see `trading-assistant`), that becomes the first concrete example of Littlebird's context feeding into — and eventually being fed by — the agent fleet. The intended end state is a paid-tier, tailored **end-of-session trading journaling routine** (the Morning Brief prompt above already gestures at this: "until ideally we can afford to pay for Littlebird and create a tailored end of session trading journaling routine").
3. **Public-preview lane, built by Alfred, in a future session.** Christopher wants raster-ready HTML surfaces he can share to LinkedIn/X, showcasing Fortuna and the rest of the agent fleet as built on top of Littlebird's context layer — while this repo (and whatever private data collection sits behind it) stays private. Public = shareable showcase; private = full data + context awareness.
4. **Beyond trading.** Once the trading use case is live and shareable, the plan is to showcase other ways Littlebird has been helping Christopher day-to-day, outside of trading — the Morning Brief already spans far more than trading (family, web3, recovery, PIR/community commitments), so there's real material here once the first showcase proves the pattern out.

## Scope of this repo

- **In scope:** planning notes, the Morning Brief prompt, program context, ambassador-program details as they firm up, and eventually a working outline for what the public-preview surfaces should contain.
- **Out of scope, always:** signing up for anything, accepting payment on Christopher's behalf, configuring or operating Littlebird's screen recording, or any other action requiring Christopher's own account credentials or consent in the moment. Any agent working in this repo should treat it as read/write for planning content only.

## Cross-references

- **Alfred** (`~/code/anthropas-argus-alfred`) — owns building out the public-preview lane in a future session.
- **trading-assistant** (`~/code/trading-assistant`) — where the actual trading-data showcase content lives once built (trade reviews, pattern tracker, gallery). Fortuna's domain.
- **mystarch_chief-of-staff** (`~/code/mystarch_chief-of-staff`) — Augment Intent's app-level coordination seat; may end up relevant if this ambassador work needs cross-project scheduling/coordination down the line.

---

*Established September 2026 — context capture only, no public content published yet.*
