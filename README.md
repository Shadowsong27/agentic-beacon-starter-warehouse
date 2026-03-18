# Agentic Beacon Starter Warehouse

A ready-to-use warehouse for experimenting with [Agentic Beacon](https://github.com/Shadowsong27/agentic-beacon).

## Getting Started

**1. Clone this repo locally**
```bash
git clone https://github.com/Shadowsong27/agentic-starter-warehouse.git ~/agentic-starter-warehouse
```

**2. Install Agentic Beacon**
```bash
pip install agentic-beacon
```

**3. Connect your project to this warehouse**
```bash
cd ~/my-project
abc warehouse connect --path ~/agentic-starter-warehouse
```

**4. Declare the artifacts you want and sync**
```bash
abc setup --manual   # edit .agentic-beacon/beacon.yaml to pick contexts/skills
abc sync             # copies artifacts into your project and wires your agent config
```

> **Note:** This warehouse is local-only by design. `abc contribute` requires a local git repo so your improvements can be version-controlled and shared with your team.

## What's Included

### Contexts
Pre-written boot instructions for common stacks — loaded automatically by your AI agent at session start.

| File | Description |
|------|-------------|
| `contexts/global.md` | Universal engineering standards (commits, code review, DRY) |
| `contexts/python.md` | Python conventions (type hints, Pydantic, ruff, uv) |
| `contexts/typescript.md` | TypeScript conventions (strict mode, Zod, no `any`) |
| `contexts/react.md` | React conventions (functional components, hooks patterns) |
| `contexts/go.md` | Go conventions (error handling, interfaces, formatting) |

### Knowledge
Example decisions, lessons, and facts you can build on.

### Skills
Reusable workflows available as slash commands in your agent.

## Customising for Your Team

Fork this repo and make it your own:
- Edit context files to match your team's actual standards
- Add knowledge entries as your team accumulates decisions and lessons
- Add skills for your team's recurring workflows

See the [Agentic Beacon docs](https://github.com/Shadowsong27/agentic-beacon) for the full guide.
