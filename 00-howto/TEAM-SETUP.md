# Team setup — Cursor rules

## 1. One-time (each developer machine)

1. Read Cursor docs: https://cursor.com/docs/rules and https://cursor.com/docs/skills  
2. Install **gstack** (Garry Tan):

```bash
git clone --depth 1 https://github.com/garrytan/gstack.git ~/gstack
cd ~/gstack && ./setup --host cursor
```

Skills land in `~/.cursor/skills/gstack-*/`.

3. Optional: install Karpathy as a user skill from  
   https://github.com/swarmclawai/andrej-karpathy-skills  

---

## 2. Every new Next / Node repo

From the app repo root (adjust `RULES_SRC`):

```bash
RULES_SRC="$HOME/Documents/bizfylabsbrain/rules"   # or your clone path

mkdir -p .cursor/rules

# Always
cp "$RULES_SRC/01-engineering/karpathy-guidelines.mdc" .cursor/rules/
cp "$RULES_SRC/01-engineering/practices/security.mdc" .cursor/rules/
cp "$RULES_SRC/01-engineering/practices/testing.mdc" .cursor/rules/
cp "$RULES_SRC/04-templates/AGENTS.md.example" ./AGENTS.md

# Next.js UI / App Router
cp "$RULES_SRC/02-nextjs/nextjs-app-router.mdc" .cursor/rules/

# Express API
cp "$RULES_SRC/03-nodejs/nodejs-express-typescript.mdc" .cursor/rules/

# NestJS API (instead of or in addition to Express)
# cp "$RULES_SRC/03-nodejs/nestjs-manifesto.mdc" .cursor/rules/
# cp "$RULES_SRC/03-nodejs/nestjs-anti-hallucination.mdc" .cursor/rules/
```

Then edit `AGENTS.md`: package manager, test/lint/build commands, DB, and never-dos.

Commit `.cursor/rules/` + `AGENTS.md` so the whole team shares them.

---

## 3. Optional deeper packs

Only if the team keeps making the same class of mistakes:

- Clean architecture / TDD → `01-engineering/architecture/` + `development/`  
- Extra practices → `01-engineering/practices/`  
- React depth → `02-nextjs/from-goran-react/`  
- Node depth → `03-nodejs/from-goran/`  
- Next 15 + Supabase security → `02-nextjs/nextjs15-supabase-security.mdc`  

**Rule of thumb:** if Cursor keeps ignoring a rule, the pack is too big. Prefer fewer always-on rules.

---

## 4. Daily workflow

| When | Use |
|------|-----|
| Ambiguous product idea | gstack `/office-hours` |
| Before coding a feature | `/plan-eng-review` |
| Before PR merge | `/review` |
| On staging | `/qa <url>` |
| Shipping | `/ship` |
| Bug hunt | `/investigate` |

Karpathy guidelines (in `.cursor/rules`) keep every edit simple and surgical automatically.
