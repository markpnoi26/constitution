# Constitution

Rules for an AI coding agent, kept in the repo the agent works in.

[`CONSTITUTION.md`](https://github.com/markpnoi26/constitution/blob/master/CONSTITUTION.md)
is the whole thing — one file, readable in a few minutes. Point your agent at it and it is bound
by it.

## Why

An agent forgets. Every new session starts cold, so it drifts back to its defaults: long
explanations, abstractions for needs that never arrive, files you did not ask for, a changelog
nobody reads. Telling it "be brief" works until the context window rolls over.

Putting the rules in the project fixes that. They load at the start of every session, they
outrank the agent's own judgment, and only you can change them.

## What's in it

| Article | The rule, in short |
| --- | --- |
| I — Authority | You amend it. The agent may propose, never enact. |
| II — Communication | Shortest complete answer. Explained like I'm fifteen. No word blobs. |
| III — Construction | Build the smallest thing that runs. Complexity is earned, not pre-paid. |
| IV — Code | Clear beats fast. Names spelled out. No function that isn't needed. |
| V — History | Git is the memory. No changelogs, no progress files. |
| VI — Enforcement | Check the plan against the rules first. Cite the violation and stop. |
| VII — Amendment | Changes are appended and dated, never inserted or rewritten. |

The file is the authority; this table is just a map of it.

## Adopting it

**One project.** From the project's root:

```
curl -O https://raw.githubusercontent.com/markpnoi26/constitution/master/CONSTITUTION.md
```

Then add this line to that project's `CLAUDE.md`:

```
@CONSTITUTION.md
```

**Every project at once.** Clone the repo somewhere permanent:

```
git clone https://github.com/markpnoi26/constitution.git ~/code/constitution
```

Then import it by absolute path from `~/.claude/CLAUDE.md`:

```
@/home/you/code/constitution/CONSTITUTION.md
```

One copy, one source of truth, amended in one place.

To pick up later changes: `curl -O` again, or `git pull` in the clone.

The `@` line needs a real file on disk — it does not take a URL. That is why you download first.

## Amending it

Append to the Amendments section at the bottom of the file, with the date and the Article it
touches. Nothing else ratifies a change — not an agreement in chat, not what a previous session
did.
