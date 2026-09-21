# Garry Tan — gstack

gstack is a **skill factory** (slash commands), not a pile of always-on `.mdc` rules.

**Upstream:** https://github.com/garrytan/gstack  

## Install (Cursor)

```bash
git clone --depth 1 https://github.com/garrytan/gstack.git ~/gstack
cd ~/gstack && ./setup --host cursor
```

Skills install under `~/.cursor/skills/gstack-*/`.

## Why we don’t vendor the full repo here

gstack is large and updates often. Machines should install from upstream so `/review`, `/qa`, `/ship`, etc. stay current.

## Included here

- `gstack-AGENTS-digest.md` — short ethos digest you may append to a project `AGENTS.md` if you want gstack voice without full install.

## Team must-use commands

| Command | Purpose |
|---------|---------|
| `/office-hours` | Product interrogation before building |
| `/plan-eng-review` | Architecture / test plan |
| `/review` | Pre-merge PR review |
| `/qa` | Browser QA on a URL |
| `/ship` | Ship / PR flow |
| `/investigate` | Root-cause debugging |
| `/cso` | Security-oriented pass (when available) |
