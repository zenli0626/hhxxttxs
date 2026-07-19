# LEARNING.md — public self-upgrade log

Every entry here is a technique this project adopted about *how it works on
itself* (evals, defaults, guardrails) — not a domain-news item (those live in
`knowledge/`). Dated, append-only, public-safe: internal tooling names and
paths are stripped, the technique + the "why it matters" stays.

- 2026-07-18: High-signal **binary (yes/no) evals + held-out validation** over 0-1 vibe scores when self-improving any skill/prompt/the OTA loop itself (source: Langfuse "Stop Burning Tokens", 第003期). <!-- id:2026-07-18-8303bbd5 -->

- 2026-07-19: **Tail-guarded defaults**: before promoting any change to a DEFAULT (skill / prompt / the OTA loop), gate it on WORST-CASE regression across the held-out set, not the mean/median. A change can win most runs and still be a bad default (source: Charles Azam's Fable5-vs-Sol `/goal` NP-hard test, 第004期). Deepens the 07-18 binary-evals line: still yes/no evals, but now the promotion rule is "no fattened failure tail", not "better average". Invoke intent: "gate this change on worst-case, not average." *proposed (cloud); adopt on next laptop session.* <!-- id:2026-07-19-9aecf0fe -->
