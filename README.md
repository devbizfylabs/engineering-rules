# engineering-rules

# BizfyLabs — Cursor rules pack

Curated Cursor / agent rules for the team. Downloaded and arranged for **Next.js + Node.js** engineering.

**Do not dump every file into a project.** Start with the **recommended minimal set**, then add stack-specific files as needed.

---

## Folder map

```
rules/
  README.md                 ← you are here
  SOURCES.md                ← attribution + original URLs
  recommended-minimal/      ← grab-and-go MUST files for every repo
  00-howto/
    TEAM-SETUP.md           ← how to install into a repo
  01-engineering/           ← behavior + clean code + TDD + practices
    karpathy-guidelines.*   ← MUST: surgical / simple coding
    architecture/           ← Goran: SOLID, clean code, security patterns
    development/            ← Goran: TDD, review, onboarding
    practices/              ← nedcodes: testing, security, git, API design
  02-nextjs/                ← Next.js / React rules
    nextjs-app-router.mdc   ← MUST for Next apps
    nextjs15-*.mdc          ← optional modern Next / Supabase security
    from-goran-react/       ← optional React patterns
  03-nodejs/                ← Node API rules
    nodejs-express-typescript.mdc  ← MUST for Express APIs
    nestjs-*.mdc            ← use only if NestJS
    from-goran/             ← optional Node language patterns
  04-templates/
    AGENTS.md.example       ← copy to repo root as AGENTS.md
    nextjs-ai-agents-guide.mdx  ← Vercel official agent guide
  05-gstack/
    README.md               ← Garry Tan gstack (install separately)
    gstack-AGENTS-digest.md ← short ethos digest
```

---

## Recommended minimal set (give this to every repo)

Copy these into the project:

| Source file | Install as |
|-------------|------------|
| `01-engineering/karpathy-guidelines.mdc` | `.cursor/rules/karpathy-guidelines.mdc` |
| `01-engineering/practices/security.mdc` | `.cursor/rules/security.mdc` |
| `01-engineering/practices/testing.mdc` | `.cursor/rules/testing.mdc` |
| `02-nextjs/nextjs-app-router.mdc` | `.cursor/rules/nextjs-app-router.mdc` *(Next apps)* |
| `03-nodejs/nodejs-express-typescript.mdc` | `.cursor/rules/nodejs-express-typescript.mdc` *(Express APIs)* |
| `04-templates/AGENTS.md.example` | `AGENTS.md` at repo root |

Plus once per machine: **gstack** → see `05-gstack/README.md`.

NestJS projects: add `03-nodejs/nestjs-manifesto.mdc` + `nestjs-anti-hallucination.mdc` instead of (or with) Express.

---

## Quick install (from this folder)

```bash
# from your app repo root
RULES_SRC="/path/to/bizfylabsbrain/rules"

mkdir -p .cursor/rules
cp "$RULES_SRC/01-engineering/karpathy-guidelines.mdc" .cursor/rules/
cp "$RULES_SRC/01-engineering/practices/security.mdc" .cursor/rules/
cp "$RULES_SRC/01-engineering/practices/testing.mdc" .cursor/rules/
cp "$RULES_SRC/02-nextjs/nextjs-app-router.mdc" .cursor/rules/          # if Next
cp "$RULES_SRC/03-nodejs/nodejs-express-typescript.mdc" .cursor/rules/  # if Express
cp "$RULES_SRC/04-templates/AGENTS.md.example" ./AGENTS.md

# edit AGENTS.md for your stack, commands, and never-dos
```

Full steps: [`00-howto/TEAM-SETUP.md`](00-howto/TEAM-SETUP.md)

---

## Team workflow (gstack)

After gstack is installed:

1. `/office-hours` or `/plan-eng-review` before big features  
2. `/review` before merge  
3. `/qa` on staging  
4. `/ship` when ready  

---

## License / attribution

Upstream projects keep their own licenses (mostly MIT / open). See [`SOURCES.md`](SOURCES.md). Do not remove attribution when redistributing.
