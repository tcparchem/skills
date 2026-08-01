# Skills

Reusable Codex skills for focused, offline-first workflows.

## Included

- `teach/` — creates focused, self-contained HTML lessons with concrete examples, interactive visualizations when useful, accessible controls, syntax-highlighted code, practice, and five transfer-oriented quiz questions.

The `teach` skill is designed for concept lessons rather than code-diff explanation. It can use a background → intuition → mechanism → practice → quiz narrative when that structure fits the learner’s goal.

## Install the teach skill

### From GitHub

Clone this repository, then copy the skill into your Codex skills directory:

```sh
git clone https://github.com/<your-github-user>/skills.git
mkdir -p ~/.codex/skills
cp -R skills/teach ~/.codex/skills/teach
```

If you use a custom `CODEX_HOME`, install it under `$CODEX_HOME/skills/teach` instead. Restart or refresh Codex after installation so it discovers the skill.

### From an existing checkout

```sh
mkdir -p ~/.codex/skills
cp -R teach ~/.codex/skills/teach
```

On Windows PowerShell, the equivalent is:

```powershell
New-Item -ItemType Directory -Force "$HOME\.codex\skills" | Out-Null
Copy-Item -Recurse -Force .\teach "$HOME\.codex\skills\teach"
```

## Use it

Ask Codex to “teach me [a concept]” or invoke `$teach` directly. The skill produces a dated, self-contained HTML lesson. It uses only inline CSS and JavaScript, so the lesson works offline and has no runtime dependencies.

## Development and validation

The skill source is [`teach/SKILL.md`](teach/SKILL.md). Validate it with the Codex skill validator when available:

```sh
python3 /path/to/quick_validate.py teach
```

See [`CREDITS.md`](CREDITS.md) for attribution and provenance.
