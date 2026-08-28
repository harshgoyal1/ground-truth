# Ground Truth

**An evidence-based self-review, generated from your own work — not your own opinion of it.**

Most AI career advice is a horoscope. You describe yourself, the model flatters you back.

Ground Truth inverts that. It points your AI assistant at the things that cannot flatter you —
your commit history, your authorship split, your uncommitted work, your stale projects, your
session history, your CV — and asks one question:

> **Does what you claim match what you actually did?**

It works in any AI coding assistant. It runs entirely on your machine.

---

## What it finds

Real examples of the class of finding this produces:

- *"Your CV says 'my own platform'. Git says 83 of 223 commits are yours and the repo belongs to
  a colleague. That claim dies the moment an interviewer asks for the link."*
- *"Your flagship project has 74 commits in July and 0 in August — it went quiet exactly when you
  started marketing it."*
- *"Your CV undersells you. Nothing on it says you write production full-stack code, and your
  commit history says you do."*
- *"Client progress reports and personal tax documents are in the same folder."*

Compliments are cheap. These are the sentences that change what you do next week.

## What makes it different

| Typical AI self-assessment | Ground Truth |
|---|---|
| You describe yourself | It reads your artifacts |
| Optimised to feel good | Explicitly anti-flattery |
| Generic advice | Cites file paths, commit counts, dates |
| Strengths-heavy | Ranked by career damage |
| Confirms what you believe | Names your blind spots, both directions |

## Quick start

Open your AI coding assistant in a directory where your work lives, and paste
[`PROMPT.md`](PROMPT.md).

That's it. No install, no dependencies, no account.

### Claude Code (as a skill)

```bash
git clone https://github.com/harshgoyal1/ground-truth
cp -r ground-truth/.claude/skills/ground-truth ~/.claude/skills/
```

Then just ask: *"run ground truth on me"*.

### Other assistants

| Assistant | How |
|---|---|
| **Cursor** | Paste `PROMPT.md` into chat, or save as a project rule |
| **Codex CLI** | Paste `PROMPT.md` into a session |
| **Gemini CLI** | Paste `PROMPT.md` into a session |
| **Copilot Chat** | Paste `PROMPT.md` (agent mode, so it can run git commands) |
| **Anything else** | Paste `PROMPT.md`. It is plain English. |

**Requirement:** the assistant needs to run shell commands (`git log`, `find`) and read local
files. The git-evidence half — which produces most of the findings — works everywhere.
Reading past AI session history is assistant-specific and optional.

## Privacy

- **Everything stays local.** No servers, no telemetry, no account. The only thing leaving your
  machine is your normal conversation with your own AI assistant.
- **The output is private.** It is designed to be blunt. It will surface things you would not
  paste into a team channel. Keep it that way.
- **Run it on yourself.** Not on a colleague's machine, not on someone else's repos, not as a
  covert performance-management tool. Pointing this at someone who did not ask for it is
  surveillance, not coaching.
- Managers: share it, do not collect it. It works because it is private. The moment people think
  the output is read by someone else, they will soften the prompt and it stops being useful.

## Honest limits

- It sees what is on the machine. Work in other systems (Jira, Confluence, a company monorepo you
  do not have locally) is invisible to it.
- Commit counts are a weak proxy for contribution. Architects and reviewers commit less than
  implementers. The prompt is told this, but read its conclusions with judgement.
- It can be wrong. It is a mirror, not a verdict. Argue with it — with evidence.
- It is deliberately harsh. If you are in a bad place, this is not the tool for today.

## Contributing

Useful additions: session-history paths for assistants beyond Claude Code, better evidence
commands, translations. Open a PR.

## License

MIT
