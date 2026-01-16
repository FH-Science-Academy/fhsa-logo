# Contributing to the FHSS IMSA Logo Repository

This guide explains the expected folder workflow, required assets, and the tools you need to work with the logo files.

## Git LFS (required for image assets)

This repository tracks PNG and SVG logo files with Git LFS. Install Git LFS before adding, updating, or pulling image assets; otherwise you will only see pointer files and pushes will fail.

Install and initialize (run once per machine):

- Windows (PowerShell):
	```powershell
	winget install Git.GitLFS
	git lfs install
	```
- macOS (Homebrew):
	```bash
	brew install git-lfs
	git lfs install
	```
- Linux (apt example):
	```bash
	sudo apt install git-lfs
	git lfs install
	```

After cloning

```bash
git clone <repo-url>
cd fhsa-logo
git lfs install
git lfs pull
```

Checks

- `git lfs ls-files` — list tracked assets
- `git lfs status` — verify LFS state

If you see small text pointer files starting with `version https://git-lfs.github.com/spec/v1`, run `git lfs pull` to fetch the real images.

## Workflow overview

- `version-current/` holds the production-ready logo set.
- `version-next/` is the active working copy for upcoming changes.
- `version-template/` is the clean starting point you copy to create a new working version.
- `archive/version-YYYY-MM-DD/` stores prior releases (use ISO dates for clarity).

## Release steps

1. Archive the existing `version-current/` to `archive/version-YYYY-MM-DD/`.
2. Copy `version-template/` to `version-next/` (or directly to `version-current/` if no WIP stage is needed).
3. Make edits in `version-next/` until ready.
4. Promote `version-next/` to `version-current/` (replace/move the folder).
5. Update links or docs if paths change.

## Required files (per version)

Every version must contain all of these files:

- `primary/source/logo-sa.svg`
- `primary/exports/logo-sa.svg`
- `primary/exports/logo-sa.png`

## Notes and conventions

- Keep file names and paths identical across versions; external references depend on them.
- Prefer ISO dates (`YYYY-MM-DD`) in archive folder names for easy sorting.
- If you add new variants, mirror the structure under `variants/` with `source/` and `exports/`.

## Communication

For brand/usage questions, contact ahn_j@surreyschools.ca.
For development or repo-structure questions, contact tollyzhang@gmail.com.