# Support

This is the public support channel for the **MdHero** desktop application.

## Where to report

File issues in the **public** docs repository:

- <https://github.com/debmis/MdHeroDocs/issues>

The application source repository is private. This repository serves as the public-facing entry point for bug reports, feature requests, and general questions.

## Before filing

A quick sanity check that often saves a round-trip:

1. **Update to the latest version** if you can. Releases are posted at <https://github.com/debmis/MdHero/releases>.
2. **Check open issues** — your problem may already be tracked or have a workaround.
3. **Reproduce on a minimal workspace** — open a folder with just two or three small markdown files and confirm the issue still happens. This rules out workspace-specific corruption and gives a clear test case.

## What to include in a bug report

Copy this template into a new issue and fill in the gaps:

```markdown
**Version:** (Help → About in the app, or check `package.json` if running from source)
**OS:** (e.g., Windows 11 24H2 / macOS 14 Sonoma / Ubuntu 24.04)
**Install type:** (Microsoft Store / NSIS installer / DMG / AppImage / deb / `npm run dev`)

**What I did:**
1. …
2. …

**What I expected:**
…

**What actually happened:**
…

**Steps to reproduce on a fresh workspace:**
1. …

**Screenshots / screen recording (optional):**
…
```

## Feature requests

Open an issue with the `[feature]` prefix in the title. Describe the workflow it would unlock, not just the feature. "I want X" is harder to act on than "When I do A, I get B, but I want C because Z."

## What gets prioritised

MdHero is a single-developer project. Issues that:

- include a clean repro,
- affect the anchor features (markdown rendering, file watching, git diff overlay, search),
- or report a security concern,

will get the fastest response. Cosmetic polish and one-off feature ideas are tracked but slower to land.

## Security issues

If you find a security vulnerability — anything where MdHero could be tricked into reading, writing, or executing something outside the user's intent — please file the issue on this repository with the `[security]` prefix. The repo is public, so do not include exploitable payloads in the report; describe the impact and reproduction conditions, and we'll coordinate any details out of band.
