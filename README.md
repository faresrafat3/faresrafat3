# Fares Rafat

**I build the QA layer for AI agents — so a bug is caught by a test, not by a customer.**

Your agent says it passed. Nobody can prove it. I build the thing that makes
that provable: eval harnesses, handoff validation, deterministic gates, and cost
routing — the infrastructure most teams skip and then pay for in incidents.

📍 Cairo, Egypt · 🌐 Remote contract · 💬 [faresrafat3@gmail.com](mailto:faresrafat3@gmail.com)

---

## Start here — this one actually installs

```sh
git clone https://github.com/faresrafat3/agent-handoff
cd agent-handoff && ./install.sh
```

**[agent-handoff](https://github.com/faresrafat3/agent-handoff)** · Python, zero dependencies

Long agent sessions lose work silently: a summary with nothing under it, a
"next action" that executes as nothing, a checkpoint that no longer matches git.
This makes those **validation failures** instead of mysteries. Typed
schema-checked handoffs, a read-only `doctor`, and a bounded/redacted/hash-stamped
context pack for the next session. 60 tests, every guard mutation-tested.

Works with Claude Code, Cursor, Codex, Cline — anything that runs a shell command.

```
$ agent-handoff doctor --strict
"Exact next action" is not actionable: it names no path, command, id, or verification step
```

---

## The three ways agent work goes wrong

I keep coming back to these, and every engagement starts here:

1. **An agent reports success and nobody can verify it.** No eval, no regression
   test, no replayable evidence. The only QA is a human re-reading a diff.
2. **State lives in context instead of on disk.** Long sessions compact,
   identifiers get lost, and the summary quietly becomes the only copy of a
   commit hash.
3. **Failures are silent.** No failure-mode map, so the same class of bug ships
   three times and each incident is rediscovered from scratch.

The fix in all three cases is the same: make the claim **checkable**, then check
it automatically. Everything below is a version of that.

---

## What I build

| | |
|---|---|
| **Agent Reliability Audits** | Fixed-scope review of your agent pipeline. Failure-mode map, prioritized hardening plan, recorded walkthrough. |
| **Eval & Verification Layers** | Regression suites, mutation-tested gates, and CI checks that fail the build when agent behaviour drifts. |
| **Multi-Agent Orchestration** | Role-scoped write rights, veto gates, append-only state — teams of agents that can be audited. |
| **LLM Cost & Reliability Routing** | Every call to the cheapest model that can do the job, with automatic failover. |

---

## Selected work

| Project | What it is |
|---|---|
| **[agent-handoff](https://github.com/faresrafat3/agent-handoff)** · Python | Typed handoffs + validator for long agent sessions. 60 tests, no deps, installs in 3 commands. |
| **[colony-kernel](https://github.com/faresrafat3/colony-kernel)** · TypeScript | Deterministic mission-control for agent colonies: 22-stage state machine, content-addressed approvals, 67 offline tests. |
| **[crew-research-council](https://github.com/faresrafat3/crew-research-council)** · Python | Multi-agent research governance: blackboard, veto pipeline, role write-rights. Built so one agent's confident answer can't pass as a finding. |
| **[knowledge-factory](https://github.com/faresrafat3/knowledge-factory)** · Python | Compresses scattered material under a written method; 4,770-row index with one-command re-verification. |
| **[continuum](https://github.com/faresrafat3/continuum)** | Session-sealing protocol for agent harnesses; contains the portable standard above. |

---

## How I work

This is not a style preference. Each rule exists because breaking it cost real
time.

- **Records over claims.** A claim is real only if a verifier separate from the
  claimant can quote it from disk. No self-graded gates.
- **Verify before claiming.** Run the command, read the file, check the value.
  Never report "works" from reasoning alone.
- **Generated counts, never hand counts.** A hand-written number is a lie on a
  timer.
- **A gate you weakened is a gate that no longer works.** Changing a check to
  accept a record requires a failing test that proves the rejection was wrong.
- **State the limits.** Every project I ship lists what it does *not* do. A tool
  implying a guarantee it can't keep is worse than no tool.

---

## Availability

Taking **AI agent reliability** work — audits, eval layers, verification
infrastructure. Remote, Cairo-based, async-friendly.

📫 [faresrafat3@gmail.com](mailto:faresrafat3@gmail.com) · [github.com/faresrafat3](https://github.com/faresrafat3)
