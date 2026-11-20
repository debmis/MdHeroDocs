# Privacy Policy

**Effective date:** 2026-11-19
**Applies to:** MdHero desktop application (Windows, macOS, Linux), all distribution channels (Microsoft Store, direct download, GitHub releases).

## Short version

MdHero does not send telemetry or upload local Markdown files. Folder workspaces are processed on your device. Opening a GitHub pull request sends requests to GitHub to load that PR. A local Markdown preview can also load HTTPS images referenced by the document.

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
- **No MdHero accounts.** MdHero has no account or sync service. You can choose to use your existing GitHub CLI sign-in to access a private pull request.
- **No cloud storage or sync.** MdHero does not upload local workspace files or local review notes.
- **No MdHero update check.** MdHero does not check for updates itself. Loading or restoring a preview can request images referenced by the document.
- **No third-party SDKs, advertising networks, or trackers** of any kind.

## Network behaviour

- **GitHub PR review.** When you choose to open a GitHub.com pull request, MdHero sends its repository identifier and PR number to GitHub over HTTPS. It requests the PR metadata and changed-file list, then retrieves the Markdown revisions needed for the file you select. GitHub receives normal connection information such as your IP address and handles the requests under its [privacy statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement). PR content is kept in memory while the app runs. MdHero does not upload local files or post comments to GitHub.
- **Optional GitHub CLI authentication.** If you select GitHub CLI authentication, MdHero asks the installed `gh` CLI to make those requests. GitHub receives the requests under the account already configured in GitHub CLI. MdHero does not read or store the CLI's credentials. Leave the option unchecked to send unauthenticated requests for public PRs. To avoid GitHub requests from MdHero, use folder workspaces and leave the PR picker unused.
- **Embedded images.** A local Markdown preview can load HTTPS images referenced in a document. The image host receives normal connection information. Remove the external image reference or avoid opening that document to prevent the request. GitHub PR previews display image alt text without loading images.
- **External links.** Clicking an HTTP or HTTPS link opens it in your default browser. The browser handles that request.
- **Mermaid.** Diagrams in local workspaces are rendered on your device.

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

MdHero is a developer productivity tool with no audience-targeting features. MdHero does not knowingly collect personal information from children. GitHub and any image hosts are governed by their own privacy policies.

## Changes to this policy

If this policy ever changes in a way that affects what MdHero does with your data, the change will be reflected here with an updated effective date. The current effective date is at the top of this document.

## Contact

Questions about this policy can be raised as an issue on the public docs repository:

- <https://github.com/debmis/MdHeroDocs/issues>

This document is the canonical privacy policy for MdHero. Distribution-channel listings (Microsoft Store, etc.) may link to it as the authoritative source.
