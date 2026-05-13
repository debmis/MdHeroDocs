# Privacy Policy

**Effective date:** 2026-05-13
**Applies to:** MdHero desktop application (Windows, macOS, Linux), all distribution channels (Microsoft Store, direct download, GitHub releases).

## Short version

MdHero does not collect, transmit, or store any personal data. The application makes no outbound network requests of its own. Everything you do in MdHero stays on your computer.

## What MdHero does on your computer

MdHero is a local desktop application. When you use it, it:

- Reads markdown files from a folder you explicitly choose.
- Renders those files as HTML for the preview pane.
- Watches the chosen folder for file changes so the preview can refresh.
- Runs local `git` commands (against your local git installation) to compute block-level diffs against a git ref you select.
- Stores your settings (theme, recently opened folder, pane sizes) on your local disk under the operating system's standard application-data location.
- Opens external links you click in the preview using your operating system's default web browser. The browser, not MdHero, makes that network request.

## What MdHero does **not** do

- **No telemetry.** MdHero does not send usage analytics, crash reports, or any other metrics anywhere.
- **No accounts or sign-in.** There is no MdHero account system. You do not create credentials, log in, or sync anything to a server.
- **No cloud storage or sync.** Your markdown files stay where you put them. MdHero does not copy them anywhere.
- **No update check or "phone home".** The application does not contact any server on startup or in the background.
- **No third-party SDKs, advertising networks, or trackers** of any kind.

## Network behaviour

The application itself makes no outbound network requests. The two exceptions, both of which are handled by your operating system and not by MdHero, are:

1. **External links** — clicking a `http://` or `https://` link in the rendered preview opens it in your default browser. The browser, not MdHero, makes the request.
2. **Mermaid diagrams** — rendered locally inside the application from your own source; no network access required.

If you obtained MdHero through the Microsoft Store or another platform store, those stores may have their own update and telemetry mechanisms governed by their own privacy policies. MdHero itself does not participate in or augment that telemetry.

## Data stored on your device

MdHero writes the following to your operating system's user-data location:

- Application settings (theme, pane sizes, last opened folder).
- Local-only review notes you create with the in-app "Note" affordance.
- Indices (tag list, backlink graph) computed from your workspace files.

The exact location depends on installation type:

- **Windows MSIX (Microsoft Store):** `%LOCALAPPDATA%\Packages\Polestar.MdHero_*\LocalCache\Roaming\MdHero\`
- **Windows NSIS installer:** `%APPDATA%\MdHero\`
- **macOS:** `~/Library/Application Support/MdHero/`
- **Linux:** `~/.config/MdHero/`

You can delete this folder at any time. MdHero will recreate it with defaults on the next launch.

## Children's privacy

MdHero is a developer productivity tool with no audience-targeting features. It does not knowingly collect any data from any user, including children. Because the application collects no data, no special handling for users under 13 is required.

## Changes to this policy

If this policy ever changes in a way that affects what MdHero does with your data, the change will be reflected here with an updated effective date. The current effective date is at the top of this document.

## Contact

Questions about this policy can be raised as an issue on the public docs repository:

- <https://github.com/debmis/MdHeroDocs/issues>

This document is the canonical privacy policy for MdHero. Distribution-channel listings (Microsoft Store, etc.) may link to it as the authoritative source.
