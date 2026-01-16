# Contributing to the FHSS IMSA Logo Repository

This guide explains the expected folder workflow and the minimum files each version must include.

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