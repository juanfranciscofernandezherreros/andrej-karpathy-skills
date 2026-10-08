# Using Karpathy Guidelines with OpenAI Codex

This repository supports Codex through two complementary mechanisms.

## Option A: Project instructions (always applicable inside the project)

Copy [`AGENTS.md`](./AGENTS.md) into the root of the project where you run Codex:

```bash
cp AGENTS.md /path/to/your-project/AGENTS.md
```

If the destination already has an `AGENTS.md`, **merge** the guidelines into the existing file instead of overwriting project-specific instructions.

For personal, cross-project instructions, you may also merge the guidance into `~/.codex/AGENTS.md`.

## Option B: Install as a reusable Codex skill

The existing [`skills/karpathy-guidelines/SKILL.md`](./skills/karpathy-guidelines/SKILL.md) already uses the skill frontmatter (`name`, `description`) that Codex recognizes.

From the repository root:

```bash
mkdir -p ~/.agents/skills
cp -R skills/karpathy-guidelines ~/.agents/skills/
```

Alternatively, clone the repo first:

```bash
git clone https://github.com/juanfranciscofernandezherreros/andrej-karpathy-skills.git
cd andrej-karpathy-skills
mkdir -p ~/.agents/skills
cp -R skills/karpathy-guidelines ~/.agents/skills/
```

Restart Codex if the newly installed skill is not detected in your existing session. Ask Codex to use `karpathy-guidelines` when writing, reviewing, or refactoring code.

## Which should I use?

- **`AGENTS.md`**: choose this when you want the rules to apply consistently in the target project.
- **`SKILL.md`**: choose this for a portable, reusable skill that Codex can invoke for relevant coding work.
- You may use both; they intentionally share the same four principles.

## Verify the setup

1. Confirm the target project contains `AGENTS.md`, or check that `~/.agents/skills/karpathy-guidelines/SKILL.md` exists.
2. Start Codex in a small test project and ask it to make a narrowly scoped change using these guidelines.
3. Confirm the resulting diff is limited to relevant files, assumptions are surfaced, and available tests are run.

The original Claude Code plugin and Cursor configuration remain unchanged.
