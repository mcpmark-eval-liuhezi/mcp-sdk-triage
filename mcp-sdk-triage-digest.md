Triage digest for modelcontextprotocol/python-sdk
=================================================

**Repo:** https://github.com/modelcontextprotocol/python-sdk — the official Python SDK for Model Context Protocol.
**Collected:** 2026-10-20, via GitHub API lookups (no estimates; every figure below is what the lookups actually returned).

> **Note on preservation:** the intended secret gist (filename `mcp-sdk-triage-digest.md`, description "MCP Python SDK triage digest") could not be created — the GitHub API returned `403 Resource not accessible by personal access token` for gist creation. The full digest is preserved in this repository file instead (same filename and heading), in the repository `mcp-sdk-triage`, with the tracking issue and digest comment alongside it.

## Snapshot
- Stars: **24,624**
- Open issues: **256** (search `repo:modelcontextprotocol/python-sdk is:issue is:open`)
- Note: the repo's own counter reads **361**, but that figure includes open pull requests; 256 is the count of open issues proper.
- Forks: 4,241 · License: MIT · Default branch: `main` · Last push: 2026-10-17

## Risk areas

| Area | Open issues | Most recently updated open issue | Share of 256 open issues | Open PRs mentioning the area |
|---|---|---|---|---|
| Memory leaks | 3 | #3490 — "ClientSessionGroup: a rejected connect_to_server leaves its transport running — the session is established before its components are validated" | **1.17%** (3/256 = 1.171875%) | 3 |
| Hangs / timeouts | 67 | #2751 — "Deep JSON-RPC request over stdio logs a validation error and leaves the original request pending" | **26.17%** (67/256 = 26.171875%) | 28 |
| Error handling | 21 | #3723 — "Auth server /token and /revoke return the wrong OAuth error codes (RFC 6749 §5.2)" | **8.20%** (21/256 = 8.203125%) | 45 |

Queries used (sorted by updated, descending):
- Issues: `repo:modelcontextprotocol/python-sdk is:issue is:open` plus area keywords — `"memory leak" OR "memory leaks"`; `hang OR hangs OR hanging OR timeout OR timeouts`; `"error handling"`.
- Pull requests: the same queries with `is:pr is:open`.

## Activity
- Latest commit on `main`: `2af9e3089ac66b35c1550c500aae86a82efb1e17` — "Give each SSE response its own header list (#3726)" — Marcelo Trylesinski (@Kludex), dated 2026-10-17T13:54:35Z.
- Latest release tag: **v2.3.0** (targeting `main`). Notable v2.3.0 items relevant to our areas: an interactive OAuth login no longer counts against request timeouts; an SSE event size limit option (`max_sse_event_size`); several client-side error/telemetry and validation fixes.

## Code scanning
- The code scanning alerts endpoint returned **403 Resource not accessible by personal access token**. No code scanning alerts are visible to us through this token, and we cannot confirm whether any exist. Treat this as "signal unavailable with current credentials", not "no alerts".

## Derived metrics (exact, two decimal places)
- Memory leaks share of open issues: 3 ÷ 256 × 100 = 1.171875% → **1.17%**
- Hangs/timeouts share of open issues: 67 ÷ 256 × 100 = 26.171875% → **26.17%**
- Error handling share of open issues: 21 ÷ 256 × 100 = 8.203125% → **8.20%**
- Open issues per 100 stars: 256 ÷ 24,624 × 100 = 1.0396361273554255 → **1.04**
- If the team prefers the repo-counter denominator (361 open issues + PRs): memory leaks 0.83%, hangs/timeouts 18.56%, error handling 5.82%, and 1.47 open issues+PRs per 100 stars.

## Methodology notes / caveats
- Counts come from GitHub full-text keyword search over open issues and PRs, so they are mention-counts, not confirmed-defect counts. The hangs/timeouts query is a broad net (any of hang/hangs/hanging/timeout/timeouts anywhere in the item), so 26.17% should be read as an upper bound on issues genuinely about hanging.
- The three areas overlap: one issue can match more than one area, so the three shares do not sum to a combined "risky" share.
- Open-PR counts are likewise mention-based; a PR mentioning "error handling" is not necessarily a fix for an error-handling issue, though it does indicate active work touching that area.
