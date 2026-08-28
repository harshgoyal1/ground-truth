# Contributing

Ground Truth is a prompt, not a codebase. The most useful contributions are
improvements to what it looks at and how honestly it reports.

## Good contributions

- **Evidence commands** — better ways to surface truth from git, the filesystem,
  or an assistant's session history.
- **Assistant coverage** — session-history locations and setup for assistants
  beyond Claude Code. Please only add what you have actually tested.
- **Sharper ground rules** — the anti-flattery constraints are the core of this.
  If you find phrasing that produces more honest output, that is the highest-value PR.
- **Translations.**

## Please don't

- Add scoring, grades or percentages. The moment this produces a number, people
  optimise the number instead of fixing the problem.
- Soften the tone. Bluntness is the feature.
- Add anything that sends data off the user's machine.
- Add a mode for reviewing other people. This tool is for reviewing yourself;
  pointed at someone who did not ask, it is surveillance.

## Before opening a PR

Run your change on yourself first. If the output got vaguer or more flattering,
the change is wrong.
