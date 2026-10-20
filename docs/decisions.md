# Architecture decisions

## 2026-10-20 — Reuse official Upwork integration, customize qualification
**Decision:** Start from the official [Upwork Agent Plugin](https://github.com/upwork/upwork-agent-plugin) for marketplace access and proposal workflow conventions. Keep personalized scoring, evidence, pricing rules, and tracking in this repository.

**Why:** Avoid duplicating supported marketplace access and reduce reliance on undocumented scraping.

**Caution:** Verify current capabilities, permissions, license, and platform requirements before use. An integration's confirmation flow is not by itself a guarantee of user approval; our workflow must enforce the explicit review boundary.

## 2026-10-20 — Human approval required for all proposal writes
**Decision:** No proposal submission, boost, withdrawal, or material edit without a fresh preview and explicit user approval.

**Why:** Connects have a cost, proposals are public-facing commitments, and job details can change.

## 2026-10-20 — Local-first and privacy-conscious
**Decision:** Keep personal portfolio details, client notes, tracker exports, and credentials out of the public repository. Use ignored local files or an approved secret store.

**Why:** The repository is public at initialization; only sanitized templates and reusable workflow rules belong here.
