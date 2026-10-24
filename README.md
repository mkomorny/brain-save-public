# Brain Save

> **Tri-Platform Agent Skill** for Claude Desktop / Code, Grok CLI, and Google Antigravity / Gemini.  
> Direct Memory Storage with Tags and Durability Flags — Directly saves new memories, architectural decisions, notes, and preferences to Second Brain with inline #tags and !durable/!state/!volatile flags.

---

## Overview

`brain-save` provides standardized capabilities across conversational AI platforms:
- Direct memory capture tool wrapper (/brain-save <text> or /remember).
- Inline #tag parsing and metadata categorization.
- Volatility flag parsing (!durable, !state, !volatile).
- Immediate confirmation reporting with newly assigned memory ID.
- Tri-platform NTFS junctions connecting Claude, Grok, and Antigravity.
- Standard documentation suite: SKILL.md, HOW_TO_USE.txt, IMPLEMENTATION_PLAN.md, and README.md.

---

## Tri-Platform Architecture

Zero duplicate code across platforms. Canonical source resides in `.agents`:
- **Canonical Source**: `C:\Users\<you>\.agents\skills\brain-save`
- **Claude**: `C:\Users\<you>\.claude\skills\brain-save` (NTFS Junction)
- **Grok**: `C:\Users\<you>\.grok\skills\brain-save` (NTFS Junction)
- **Antigravity**: `C:\Users\<you>\.gemini\config\skills\brain-save` (NTFS Junction)

---

## Documentation Suite

- [`HOW_TO_USE.txt`](HOW_TO_USE.txt): Standardized user guide and prompt templates.
- [`IMPLEMENTATION_PLAN.md`](IMPLEMENTATION_PLAN.md): Feature checklist and roadmap.
- [`App Changes Tracker.html`](App%20Changes%20Tracker.html): Interactive visual version log.
- [`SKILL.md`](SKILL.md): Agent system instructions and triggers.
