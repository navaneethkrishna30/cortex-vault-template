# Cortex vault template

A starter vault for [Cortex](https://github.com/navaneethkrishna30/cortex), shared memory for your AI agents. It gives you the folder layout, the rules agents follow and a few example notes.

## Get started

```bash
git clone https://github.com/navaneethkrishna30/cortex-vault-template ~/cortex-memory
cd ~/cortex-memory
git remote remove origin
rm memory/example-preference.md entities/example-*.md docs/example-plan.md
git add -A && git commit -m "Start my vault"
CORTEX_VAULT=~/cortex-memory cortex serve
```

Your notes are personal, and Cortex pushes the vault to every git remote it has. For a backup, add a remote of your own and keep it private.

Then write about yourself in `core/profile.md`. To make sure agents load Cortex, copy the line in `AGENTS.md` into each project's agent file.

## What goes where

```text
core/       Rules, relation types and your profile. Agents get these every session and can't edit them.
memory/     One small file per fact. Agents get an index of these every session.
entities/   Short cards for things whose state changes: projects, machines, people.
docs/       Plans, research and detail. Agents read these only when asked.
logs/       Append-only daily notes, debriefs and raw chats.
.archive/   Notes you've retired. Cortex never searches them.
```

## How agents behave

[`core/rules.md`](core/rules.md) sets how agents use the vault, and [`core/relations.md`](core/relations.md) lists the links they can make between notes. Both are yours to change.

The examples show the note formats before you delete them:

- [`memory/example-preference.md`](memory/example-preference.md): a one-line memory
- [`entities/example-project.md`](entities/example-project.md): a card with relations and a History
- [`entities/example-database.md`](entities/example-database.md): a card that shows backlinks
- [`docs/example-plan.md`](docs/example-plan.md): a longer doc

Search settings live in [`.cortex/config.toml`](.cortex/config.toml). Notes are embedded locally by default, and the file explains how to switch to Voyage.

## License

[MIT](LICENSE)
