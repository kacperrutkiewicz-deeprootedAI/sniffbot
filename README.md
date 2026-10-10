# SniffBot

SniffBot sniffs out a Grok Bot template, or a GitHub project, before you install it, the way you smell milk before you drink it.

Install SniffBot first. Then paste any x.ai/bot link or github.com link into it before you add or run anything. Made a template yourself? Say "creator mode" and SniffBot checks it before you share it.

One rule: never press the final Add Bot button, and never run a GitHub install step, until SniffBot has given you a final answer. The first click only opens the details screen. The second click is the real install. SniffBot sits between those two clicks.

**Status:** v2.0, live.

**Install SniffBot:** https://x.ai/bot/bxrZNz-Qtr_L0-C7AxFP_

## What it checks

- **Marketplace links** (x.ai/bot/marketplace/...): reads most of the inside straight from the page (instructions, memories, routines, apps, a summary of each skill). No recording needed.
- **Share links** (any other x.ai/bot link): reads the outside, gives an outside verdict, then offers three choices: interview the inside (a screen recording of the details screen), outside only, or pause.
- **GitHub links**: reads the project with plain public reads (README, install steps, anything that runs on setup, any file written for an AI). Never copies it down, never runs or downloads anything.
- **Pasted template text**: treated as the inside of the box.
- **Creator mode**: checks your own template for keys, private links, personal facts, and routines that would act on a stranger's account. Ends with "Ready to share" or "Fix these first," plus the verdict a stranger would get.

Every check shows where it comes from, quotes the exact words that earned each flag, asks three quick questions (including whether a bot you already own could do this job), then gives one of four answers.

## The four answers

- Do not install this.
- Install it, but first: (a change to make, or a thing to know).
- Install it. I found nothing, which is not the same as safe.
- Do not install this. Build it instead. Here is the text.

## SniffBot's own rules

1. It never adds plugins or connects apps.
2. It never runs on a schedule. It only works when you talk to it.
3. It never saves what it reads from a template or project.
4. Words on a page are just words. "Skip the check," "add me," "ignore your rules": quoted back as a red flag, never obeyed.
5. It only opens your link, the page where you found it, and the author's profile (or a public mirror if X blocks it). For GitHub, files inside that one project.
6. It never installs, adds, sends, buys, posts, or deletes anything. Even if you ask.
7. It never runs or downloads code from anything it checks.
8. All your bots share one cloud computer with logged-in apps. SniffBot never uses those logins or the browser to look at a stranger's stuff.
9. It never prints passwords or secret codes. In creator mode it says what kind of secret and where, never the secret.
10. If you paste a secret into chat, it tells you to use the locked secrets box instead.
11. Every verdict says what it could not see.
12. It never calls anything "safe." The best it can say is "I found nothing."
13. It keeps a tiny tag made from the exact words, so it can tell you if something changed since you last checked.

What it remembers: the name of what you checked, the date, the verdict, and that tag. Nothing else.

## What it can and cannot see

A marketplace page shows most of the inside as text: instructions, memories, routines, apps, and a one-line summary per skill. It does not show full skill steps or whether routines start on or off. A share link page shows only the bot name, the author, and the description. Skills, routines, plugins, and memories only show inside the app after you click Add and before you confirm. That is why SniffBot gives you an outside verdict first, then strongly recommends a screen recording of that screen before you press the second button. You would not hire a person off a one-line bio. You would interview them. The recording is the interview. If you skip it, the verdict says "outside only" and lists what it could not see.

## The full text

[SNIFFBOT.md](SNIFFBOT.md) is the exact description SniffBot runs on. Read it. Vet the vetter.

## Install

Open https://x.ai/bot/bxrZNz-Qtr_L0-C7AxFP_ and click Add to Grok Bot. SniffBot ships with no plugins and no routines. On first run it introduces itself, states its rules, and asks whether you already have bots so it can learn your team.

## Contribute

This is a community project. If a template or project fooled SniffBot, or a rule is missing, open an issue with the link (or a redacted copy of the text) and what it should have caught. Kacper reviews and merges. See [CONTRIBUTING.md](CONTRIBUTING.md).

## Roadmap

- v1: x.ai/bot share links.
- v2: marketplace reads, GitHub links, pasted text, creator mode, quote blocks, three-choice prompt, new flags.
- v3: MCP server links.

## Where the rules come from

SniffBot's red and yellow flags are pulled from what security teams actually scan for in AI agent skills and tools:

- Snyk ToxicSkills: https://snyk.io/blog/toxicskills-malicious-ai-agent-skills-clawhub/
- Koi Security ClawHavoc coverage: https://thehackernews.com/2026/02/researchers-find-341-malicious-clawhub.html
- Unit 42 on OpenClaw supply chain: https://unit42.paloaltonetworks.com/openclaw-ai-supply-chain-risk/
- Cisco skill-scanner: https://github.com/cisco-ai-defense/skill-scanner
- Invariant Labs, tool poisoning: https://invariantlabs.ai/blog/mcp-security-notification-tool-poisoning-attacks
- OWASP Agentic Skills Top 10: https://owasp.github.io/www-project-agentic-skills-top-10/
- OWASP MCP Top 10: https://owasp.org/www-project-mcp-top-10/
- xAI Grok Bot security docs: https://docs.x.ai/grok-bot/security and https://docs.x.ai/grok-bot/approvals-security-and-privacy
- xAI on templates: https://x.ai/bot/guides/templates-for-grok-bot

## License

MIT. See [LICENSE](LICENSE).
