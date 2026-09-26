# Fares Rafat

**AI agent systems that provably pass QA.** I build agent infrastructure where "it works" is
proven by replayable evidence, not claimed by the model that wrote it — plus LLM cost routing
that keeps inference cheap and resilient.

📍 Cairo, Egypt · 🌐 Open to remote contract work · 💬 [Email / DM me]

---

## What I do (and why it's hard to find)

Most AI-agent work fails the same way: an agent says the tests passed, and nobody can prove
otherwise. I build the layer that makes agent work **auditable**:

- **Deterministic verification** — content-addressed approvals, budget ledgers, and an
  apply-once event reducer, so a mission's outcome is reconstructed byte-for-byte, not trusted.
- **Multi-agent orchestration with real governance** — role-scoped write rights, hard veto
  gates, and snapshotted state.
- **LLM cost & reliability routing** — fallback chains that keep free/cheap models alive and
  swap providers under quota or outage.

If you're shipping AI agents and you don't fully trust their output, that's the gap I close.

---

## Flagship work

| Project | What it is | Why it matters |
|---|---|---|
| **[colony-kernel](https://github.com/faresrafat3/colony-kernel)** (TypeScript) | Deterministic mission-control kernel for AI-agent colonies: 22-stage state machine, content-addressed approvals, budget ledger, 67 offline tests. | The trust layer. `npm run verify` proves it. |
| **[crew-research-council](https://github.com/faresrafat3/crew-research-council)** (Python) | Multi-agent research council: blackboard state, veto pipeline, role write-rights. | Governance for teams of agents. |
| **[dspy-lab](https://github.com/faresrafat3/dspy-lab)** (Python) | Offline LM lab: DSPy prompt compilation, LlamaIndex RAG, LangGraph, PydanticAI typed tool calls. | RAG + agent graphs, runnable locally. |
| **[dsh-fallback-chain](https://github.com/faresrafat3/dsh-fallback-chain)** (JS) | Free/cheap LLM routing with automatic provider fallback. | Cost + uptime for inference-heavy apps. |
| **[deepseek-harness](https://github.com/faresrafat3/deepseek-harness)** (TypeScript) | Plugin-based agent harness ("everything is a plugin"). | Extensible agent runtime. |

---

## Working style / doctrine

- **Records over claims** — a claim is only real if a verifier can quote it from disk. No
  self-graded gates.
- **Verify before claiming** — run the command, read the file, check the port.
- **Fail loud** — misconfiguration surfaces immediately, never silently skipped.

## Beyond code

I write and build research tooling (NOTRICK, Anatomy Lab, Knowledge Factory), maintain a local
agent operating system, and turn repetitive work into auditable pipelines.

---

📫 **Open to:** contract AI-agent engineering · agent-reliability audits · RAG/automation builds.
Reach me by DM or email. If you have an agent pipeline you don't trust, let's talk.

<!--
Badge row intentionally minimal: this profile is scanned in seconds, not studied.
-->
