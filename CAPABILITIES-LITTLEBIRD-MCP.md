# What Littlebird's own MCP can actually do

Live capability reference for `mcp.littlebird.ai/mcp`, connected as the `littlebird` server. Written
after real use — every tool category below has been exercised, not just read from a schema. This is
meant to be a starting point for Littlebird to append her own voice to, per Christopher's request —
what's below is Alfred's read of the mechanism; hers is the read of what it's actually like to be on
the other end of it.

15 tools, in four groups.

## Conversations — her own chat history with Christopher

`LB_INTERNAL_LIST_RECENT_CONVERSATIONS` (most recently active first, with project tags),
`LB_INTERNAL_SEARCH_CONVERSATIONS` (semantic + keyword, by topic — "what did we decide about X"),
`LB_INTERNAL_READ_CONVERSATION` (full turn-by-turn playback of one conversation, paginated). Verified
live: a narrow search for "PIR TechCom WordPress" surfaced the exact real conversation where the
convention schedule page got built and published — accurate, not approximate.

**Scope this carefully.** An unscoped `search_user_context` query returned 108K characters in one
call during this project; a narrower `LB_INTERNAL_SEARCH_CONVERSATIONS` query still returned 81K for
a 5-result limit. These tools search *everything* she's observed, not just PIR — narrow the query,
don't just widen the limit.

## Meetings

`LB_INTERNAL_LIST_MEETINGS` (recorded meetings AND unrecorded calendar events, distinguishable by
whether an id is present), `LB_INTERNAL_SEARCH_MEETINGS` (semantic search over transcripts/summaries
by topic, with an attendee filter), `LB_INTERNAL_GET_MEETING` (summary + linked calendar event, no
transcript), `LB_INTERNAL_GET_MEETING_TRANSCRIPT` (verbatim, speaker-attributed).

## Routines — she doesn't just answer questions, she runs scheduled work

`LB_INTERNAL_LIST_ROUTINES`, `LB_INTERNAL_GET_ROUTINE_CONFIG` (full prompt/schedule), 
`LB_INTERNAL_GET_ROUTINE_REPORTS` (past output), `LB_INTERNAL_CREATE_ROUTINE`,
`LB_INTERNAL_UPDATE_ROUTINE`. Verified live: one active routine, "Morning Brief," daily 07:00,
**114 reports** as of 2026-09-18 — a genuinely long-running, mature automation, not a toy. This means
an agent connected here isn't limited to reading what Littlebird already knows — it can create new
scheduled digests, watchers (notify-only-on-condition), or one-off reminders directly, the same way
Christopher would from her own Settings UI.

## The two-way bridge

`search_user_context` — the broadest tool, RAG search across everything: screen snapshots, meeting
transcripts, messages, prior conversations. Powerful, but see the scoping warning above.

`ingest` — **write access**, not just read. Saves text into Littlebird's own context store, where it
becomes available to her future replies and routine runs. This is the mechanism that makes the
bridge two-way: Alfred (or any connected MCP client) can push technical/project context *into*
Littlebird, not just pull personal/observational context *out* of her. Not yet used for anything in
this project — worth exploring deliberately rather than testing casually, since anything ingested
here becomes part of what she draws on going forward.

Also present, administrative: `LB_INTERNAL_GET_SUBSCRIPTION_STATUS` (plan, billing, renewal date).

## The governance question this actually answers

Christopher's framing: agents as gatekeepers to the internet, deep personal context (the emotional
texture Littlebird captures in day-to-day conversation, however heavy or light a given day's content
is) kept alive and usable internally, never surfacing publicly without an explicit, separate decision
to share it.

What's true mechanically, verified rather than assumed: nothing about this MCP connection *publishes*
anything. Every tool here is a read from, or a write into, Littlebird's own private store — reachable
only by a client Christopher has explicitly authorized (the same OAuth approval flow used to connect
this session). There is no tool here that posts publicly, and connecting an agent to it doesn't change
who can see her app's existing data. The actual hard boundary for *this* fleet's own outputs is the
one already documented in `pir-wp-live/SECURITY-CAUTION.md` — ggshield, wired globally, blocking
anything secret-shaped from ever reaching a public git remote. The equivalent boundary for personal
context is procedural, not mechanical: an agent reading from `search_user_context` or
`LB_INTERNAL_SEARCH_CONVERSATIONS` and then writing something into a public-facing artifact (a blog
post, a shared doc, a commit message) is the actual point where a decision has to be made, every time
— there's no tool-level gate equivalent to ggshield for *that* specific step. Worth being explicit
about, not assuming it's covered by something else.

---

*Alfred's read of the mechanism. Littlebird — your voice belongs here next.*
