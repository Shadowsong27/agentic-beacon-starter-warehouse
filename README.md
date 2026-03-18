# Agentic Beacon Starter Warehouse

A ready-to-use example warehouse for experimenting with [Agentic Beacon](https://github.com/Shadowsong27/agentic-beacon).

It comes with pre-written context files for common stacks (Python, TypeScript, React, Go) so you can try the full sync workflow without writing anything from scratch.

> **This is a local-only warehouse.** Clone it to your machine and connect via `abc warehouse connect --path`. Remote connections are not supported — this is by design, so that `abc contribute` can version-control your improvements via git.

## Getting Started

**1. Install the Agentic Beacon CLI**

```bash
# Recommended
uv tool install agentic-beacon

# Or with pipx
pipx install agentic-beacon

# Verify
abc --version
```

> See the [full installation guide](https://github.com/Shadowsong27/agentic-beacon?tab=readme-ov-file#installation) for offline/bundle installs.

**2. Clone this warehouse**

```bash
git clone https://github.com/Shadowsong27/agentic-beacon-starter-warehouse.git ~/agentic-beacon-starter-warehouse
```

**3. Connect your project**

```bash
cd ~/my-project
abc warehouse connect --path ~/agentic-beacon-starter-warehouse
```

**4. Declare what you want and sync**

```bash
abc setup --manual   # creates .agentic-beacon/beacon.yaml — edit to pick contexts/skills
abc sync             # copies artifacts into your project and wires your agent config
```

## What's Included

### Contexts

Pre-written boot instructions loaded automatically by your AI agent at session start.

| File | Description |
|------|-------------|
| `contexts/global.md` | Universal engineering standards (commits, code review, DRY, testing) |
| `contexts/python.md` | Python conventions (type hints, Pydantic, ruff, uv) |
| `contexts/typescript.md` | TypeScript conventions (strict mode, Zod, no `any`) |
| `contexts/react.md` | React conventions (functional components, hooks patterns) |
| `contexts/go.md` | Go conventions (error handling, interfaces, formatting) |

### Knowledge

Example structure for capturing decisions, lessons, and facts — ready for you to populate.

### Skills

Includes the `record-knowledge` skill for systematically capturing new knowledge during agent sessions.

## Day-to-day Workflow

Once connected and synced, the ongoing loop is:

```
1. abc sync        — pull latest artifacts from the warehouse into your project
2. code with agent — agent uses the synced contexts, knowledge, and skills
3. abc delta       — see what has drifted locally
4. abc contribute  — promote valuable changes back to the warehouse
```

## Customising for Your Team

Fork this repo and make it your own:

- Edit context files to reflect your team's actual standards
- Add knowledge entries as decisions and lessons accumulate
- Add skills for your team's recurring workflows
- Push to your own git host and share the clone URL with your team

See the [Agentic Beacon docs](https://github.com/Shadowsong27/agentic-beacon) for the full guide.
