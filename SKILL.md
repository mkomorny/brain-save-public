---
name: brain-save
description: >-
  Directly saves a new memory to your Second Brain. Use when the user types /brain-save 
  or /remember and wants to store a decision, note, preference, or fact. 
  Executes immediately (direct command invocation conveys user permission).
  Supports inline #tags and !durable|!state|!volatile flags.
---

# Brain Save — Save a Memory (`/brain-save`)

## When invoked

Direct user invocation of this command carries explicit user authorization. **Execute immediately** by calling the `second-brain` MCP `remember` tool, then confirm what was saved to the user.

## Syntax

```
/brain-save <text> [#tag1 #tag2] [!durable|!state|!volatile]
```

## Parsing Rules

- Extract `#tags` from the text (e.g., `#live-actions`, `#decision`, `#task`)
- Extract volatility flag: `!durable` (permanent), `!state` (can change), `!volatile` (temporary). Default: `!state`
- Set `source: "antigravity"` (or `"claude"`, `"grok"` depending on active platform)

## Execution

Call `remember` with:
- `text`: Clean memory text
- `tags`: Extracted array of tags
- `volatility`: Extracted volatility string
- `source`: Active platform

Report confirmation to the user with the new entry ID and saved details.

## Examples

```
/brain-save Chose WebView2 for desktop UI #live-actions #decision !durable
/brain-save Need to test OSC reconnection logic #live-actions #task !state
/brain-save Prefer dark themes with green accent colors #preferences !durable
```
