# tikoci/.github

This is the special public `.github` repository for the `tikoci` organization.

## What this repo is for

GitHub uses this repository for **organization-wide default community health files** when an individual repository does not define its own copy. This is the right place to keep shared public defaults such as:

- `CONTRIBUTING.md`
- `CODE_OF_CONDUCT.md`
- `SECURITY.md`
- `SUPPORT.md`
- issue templates / pull request templates
- `FUNDING.yml`
- `GOVERNANCE.md`

Those defaults can be used by both public and private repositories in the organization, but this special `.github` repository itself needs to be **public** for the normal org-wide fallback behavior.

## What this repo is **not** for

This repository is **not** an automatic org-wide source for repository-local Copilot instruction files.

The following files only apply when Copilot is operating in the repository that actually contains them:

- `.github/copilot-instructions.md`
- `.github/instructions/**/*.instructions.md`
- `AGENTS.md`
- `.github/workflows/copilot-setup-steps.yml`

Putting those files in `tikoci/.github` does **not** cause VS Code, Copilot CLI, or other repositories' local Copilot experiences to automatically inherit them.

## Copilot behavior summary

### GitHub.com

GitHub supports **organization custom instructions** from the organization settings UI:

`Organization Settings` → `Copilot` → `Custom instructions`

Those organization instructions currently apply to GitHub.com Copilot Chat, Copilot code review, and Copilot cloud agent.

### VS Code

VS Code reads repository custom instruction files from the **currently opened repository/workspace**. It does not automatically look in this special `tikoci/.github` repository unless you are actually working inside this repository.

### Copilot CLI

Copilot CLI also reads repository custom instruction files from the **current repository / working directory**. It does not automatically inherit instruction files from this special repository for other repos.

## Practical usage for tikoci

- Keep shared **GitHub default community files** here.
- Keep only **public-safe** guidance here.
- If a Copilot instruction should affect a specific repository in VS Code or Copilot CLI, add that instruction to that repository too.
- If a Copilot instruction should be organization-wide on GitHub.com, configure it in the organization's Copilot settings.

## Maintenance note

This repository replaces the earlier assumption that a separate `.github-private` repository was the right place for org-wide public defaults. Shared public defaults should live here so they are maintained in one place.
