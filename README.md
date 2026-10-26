# H2O Skill — Pre-Sell Decision Architecture Engine

A Claude Skill that engineers a prospect's understanding, desires, beliefs,
objections, and decision criteria *before* any marketing content gets
written — so by the time someone reaches your offer, they're already
decided. Built to eliminate dependence on hard selling, convincing, or
sales calls.

Created by **John Hartzenberg** ([JBIX Digital](https://jbixcivils.netlify.app)),
built and iterated with Claude.

## What it does

Most marketing skips straight to writing a hook or an ad. This skill refuses
to. It forces a full diagnosis pass first — the offer itself, the customer's
real situation, their six layers of desire, their limiting beliefs, their
objections, the competitive landscape, and a battery of falsifiability
tests — and only then produces content, so every sentence traces back to a
specific stage in the diagnosis instead of being generically persuasive.

**Thirteen-stage workflow (A–M):**

| Stage | What it covers |
|---|---|
| A | Offer diagnosis — Promise → Mechanism → Delivery → Evidence → Outcome integrity chain |
| B–E | Customer diagnosis, six-layer desire map, failed-attempt analysis, belief ladder |
| F–H | Objection architecture, competitive/market intelligence, trust & risk architecture |
| I–J | Nine falsifiability tests, presale readiness score, buyer-journey sequencing |
| K–M | Voice/channel spec, writing the content, and a 14-point presale audit |

Every claim used in the diagnosis is labeled **KNOWN / ASSUMED / UNKNOWN /
NEEDS RESEARCH / NEEDS OPERATOR INPUT** — the skill never fills a gap with a
plausible-sounding guess.

## Structure

```
h2o-skill/
├── SKILL.md                                    # entry point, workflow, triggers
└── references/
    ├── offer-and-decision-criteria.md          # Stage A + decision criteria
    ├── desire-and-belief-mapping.md            # Stages B–E
    ├── objection-competitive-trust-risk.md     # Stages F–H
    ├── presale-sequence-tests-and-readiness.md # Stages I–J
    └── voice-channel-and-output.md             # Stages K, M
```

## Using it

**Claude Code / Claude.ai:** drop the `h2o-skill` folder into your Claude
Skills directory (`~/.claude/skills/`), or install via the Claude.ai
skills/plugin interface.

**OpenAI Codex CLI:** Codex now reads the same `SKILL.md` format natively.
Place the folder under `~/.codex/skills/` (or your project's
`.agents/skills/`) instead. The content works as-is; only the folder
location differs between the two tools.

Trigger it by name — "H2O", "run H2O", "H2O it" — or it fires automatically
on marketing-strategy requests ("presell my offer", "why isn't my marketing
converting", "map out my customer's objections").

## Non-negotiables the skill enforces

- Never fabricates scarcity, urgency, testimonials, or competitor claims.
- Never tries to fix an offer, pricing, or trust problem with better copy —
  it's required to say so instead.
- Flags any unproven major claim as a **PROOF GAP** rather than inventing
  evidence.
- Explicitly rejects "make alternatives look inferior" positioning in favor
  of establishing genuine strongest-fit-through-evidence.

## License

Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) —
see [LICENSE](LICENSE). You're free to use, adapt, and build on this
commercially, as long as you credit John Hartzenberg as the original author.
