# cortex-vault-template

A starter vault for [Cortex](https://github.com/navaneethkrishna30/cortex). Copy it, delete the examples, and point `CORTEX_VAULT` at it.

- `core/`: rules and profile, loaded every session, edited only by you
- `memory/`: one small file per fact, indexed every session
- `entities/`: short cards for anything whose state changes
- `docs/`: plans and detail, read only when asked
- `logs/`: append-only daily notes, debriefs and raw chats

Put the line in `AGENTS.md` into each project's agent file so agents load Cortex.
