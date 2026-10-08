# shared-agent-rules

Repository: [github.com/juanvs23/shared-agent-rules](https://github.com/juanvs23/shared-agent-rules)

An always-on rules system for AI coding agents (Claude Code, OpenCode, or
any tool that supports an imported instructions file). 14 rules, loaded into
every session automatically — correctness discipline, debt handling with a
proximity/justification gate, research verification instead of blind trust
in training-data memory, documentation hygiene, root-cause diagnosis instead
of blind patching, and an explicit boundary on what the agent can touch
without a human's per-change approval.

Every rule was validated cold — read in isolation, with no surrounding
context, by two models of different capability — against concrete test
cases, specifically to catch rules that sound right but get misread in
practice. Several were rewritten more than once as a result.

## Files

- `development-rules.md` — the 14 always-on rules.
- `MANIFESTO.md` — why the rules are structured the way they are (always-on
  vs. skill, capability vs. product naming, the cost tradeoff behind every
  design choice).
- `FEEDBACK-LEDGER.md` — a zero-infrastructure, append-only log of
  cross-project corrections. Mirrored on every Profile A save (dual-write
  alongside persistent memory, never instead-of — see rule 12).
- `e2e-evidence.md`, `*-template.md` — supporting mechanics referenced by
  specific rules, read on demand rather than loaded every session.
