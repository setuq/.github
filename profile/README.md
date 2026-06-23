<div align="center">

# Setuq

### Sovereign, closed-loop SOC agent — Splunk today, every SIEM tomorrow.

*Not query autocomplete. It executes, analyzes, decides, and audits — fully on-prem if you need it.*

[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](LICENSE)
[![Status](https://img.shields.io/badge/status-active-success.svg)]()
[![Made with](https://img.shields.io/badge/built%20with-FastAPI%20%2B%20React-009688.svg)]()

</div>

---

## 👋 Who we are

**Setuq** (org: [`@setuq-in`](https://github.com/setuq)) builds **agentic AI for the Security Operations Center**.

The name *Setuq* comes from **सेतु (setu)** — "bridge." That's the whole idea: a bridge between a security analyst's intent in plain language and a fully-executed, audited investigation in their SIEM — without handing their data to anyone else's cloud.

We're an open, community-driven effort focused on **autonomy you can actually own**: run it air-gapped, choose your own LLM, see every decision in an audit trail.

---

## 🎯 What we're building

A **closed-loop SOC agent**. Most "AI for SPL" tools stop at generating a query and waiting for a human. Setuq closes the loop:

```
Natural language → plan → SPL → guardrail → execute → summarize → analyze → suggest actions → decide → audit
```

You ask *"show me failed logins spiking in the last 24h,"* and Setuq plans the
investigation, writes the SPL, safety-checks it, runs it against your SIEM,
analyzes the results, recommends the next action, and records a structured
decision — **recommend / reject / escalate** — with a full audit trail.

---

## 🧱 Why it's different

We deliberately **don't** compete on NL→SPL — that's a commoditized checkbox. We win on three things incumbents structurally can't or won't copy:

| | Why it matters |
|---|---|
| 🔒 **Sovereign / air-gapped** | Run 100% locally on [Ollama](https://ollama.com). Your security data never leaves the premises — built for regulated, gov, defense, and finance SOCs that legally cannot egress. |
| 🔁 **Closed-loop autonomy *now*** | Execute → analyze → decide → audit today, not on a 2026 roadmap. An explicit decision engine, not just query suggestions. |
| 🌐 **SIEM-agnostic** | A clean client abstraction means the same pipeline targets Splunk today and Elastic / Sentinel / OpenSearch next. Not locked to one vendor. |

Plus the things you'd expect from production agent infra: **LLM fallback chains**,
**prompt-version tracing**, **OpenTelemetry + Langfuse observability**,
**customizable guardrails**, rate limiting, idempotency, and an eval harness.

---

## 📦 Inside this organisation

| Repository | What it is |
|---|---|
| **`engine`** | FastAPI agentic backend — the planner → SPL → guardrail → execute → decide → audit pipeline. |
| **`ui`** | React front-end for conversational SOC investigations with live step-by-step streaming. |
| **`splunkSetUp`** | Guides to stand up Splunk Enterprise, ingest data, and verify with SPL + dashboards. |
| **`docs`** | Architecture, strategic positioning, and competitive analysis. |

> New here? Start with the main project repo's README and the one-command
> `python bootstrap.py up` to go from zero to a running stack.

---

## 🛠️ Tech stack

**Backend:** Python · FastAPI · async pipeline architecture
**AI:** Anthropic Claude · OpenAI · Ollama (local) — pluggable with a fallback chain
**Data / SIEM:** Splunk REST API (SIEM-agnostic client abstraction)
**State:** In-memory or Redis-backed sessions
**Observability:** OpenTelemetry · self-hosted Langfuse · prompt-version hashing
**Front-end:** React + SSE streaming

---

## 🤝 Get involved

We welcome contributors, security practitioners, and the curious.

- ⭐ **Star** the repos you find useful — it genuinely helps.
- 🐛 **Issues & ideas:** open an issue on the relevant repository.
- 🔧 **Pull requests:** read each repo's `CONTRIBUTING` / `CLAUDE.md` before submitting.
- 💬 **Discussions:** use GitHub Discussions for questions and proposals.

---

## 📬 Contact

- ✉️ Email: _<setuq2026@gmail.com>_

---

## 📄 License

Setuq projects are released under the **Apache License 2.0** unless a repository states otherwise.

<div align="center">

**Setuq — the bridge from intent to action, on your terms.**

</div>
