# github-profile-readme

A [Claude](https://claude.com/claude-code) **skill** that builds a great GitHub *profile* README — the special `README.md` in the repo named after your username (`github.com/<you>/<you>`) that renders at the top of your profile page.

It was distilled from analyzing **181 popular profile READMEs** across 16 styles, so its defaults reflect what actually works at scale rather than whatever is trending. Instead of dumping every widget onto the page, it interviews you, picks **one coherent archetype** that fits your goals and how much upkeep you'll tolerate, drafts real markdown from your actual work, wires any dynamic widgets correctly, and gives you exact install steps.

## What's inside

- **`SKILL.md`** — the skill itself: the workflow, the archetype picker, and the principles.
- **`references/`** — load-on-demand depth: the nine archetypes, a copy-paste technique catalog, a tools reference with caveats, and a pitfalls + pre-publish checklist.
- **`assets/templates/`** — a ready-to-fill starter for each archetype (plus an Actions workflow for the self-updating style).
- **`scripts/build_widgets.py`** — generates consistent, theme-matched widget markdown (badges, stats cards, tech stack, typing SVG) from simple flags.

## The nine archetypes

Minimalist / Prose-First · Badge / Icon Card · Stats Dashboard · Descriptive Resume · Code-as-Bio · Self-Updating / Automated · Visual Showcase · Persona / Themed · Interactive / Game Mode.

The skill helps you pick exactly one (plus at most one accent) based on your maintenance tolerance, personality, and what you want to lead with.

## Use it

**With Claude Code:** clone into your skills directory so Claude can load it.

```sh
git clone https://github.com/{{YOUR_USERNAME}}/github-profile-readme ~/.claude/skills/github-profile-readme
```

Then just ask: *"help me make my GitHub profile README"* — the skill triggers automatically.

**Standalone:** the `references/` and `assets/templates/` files are plain markdown you can read and copy by hand, and `scripts/build_widgets.py` runs on any Python 3.

```sh
python scripts/build_widgets.py --username octocat --theme tokyonight \
  --socials linkedin:octocat,email:o@cat.dev --stats --top-langs --stack py,ts,go,docker
```

## License

[MIT](./LICENSE). Use it, fork it, build on it.
