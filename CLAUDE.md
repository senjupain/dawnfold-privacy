# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

The privacy-policy page for `dawnfold`. A single self-contained `index.html` (~100 lines, inline
`<style>`, light/dark via `prefers-color-scheme`) — no build system, no dependencies, no framework.
Deployed via GitHub Pages at `https://senjupain.github.io/dawnfold-privacy/`, from the `senjupain`
GitHub account (note: separate from the `livitaufao` GitLab account that hosts `aletheia`).

## Cross-session context (added 2026-08-08)

Every new chat is a blank conversation — it never inherits the turns from a previous chat, only the
files on disk. What loads automatically is path-based: global `CLAUDE.md` + this file (since it sits in
this directory), plus this directory's own memory folder under
`C:\Users\User\.claude\projects\<path-key>\memory\`. A session opened here does **not** automatically see
`D:\General\CLAUDE.md`'s hub content or its memory — terminal vs. desktop CLI makes no difference, only
the working directory does.

So: implementation detail belongs here, in this file. Business/roadmap/cross-app decisions (pricing,
launch timing, Akatsuki1-level calls, multi-AI workflow changes) belong in `D:\General\CLAUDE.md`
instead — if one comes up in a session working here, push it back to the hub rather than leaving it
stranded in dawnfold-privacy's local memory, where a General-hub session would never see it.

## Commands

None. Edit `index.html` directly and push — GitHub Pages serves it as-is, no build step.

## Why this exists as its own repo

This URL is the privacy-policy link submitted in Play Store listing metadata (see `STORE_LISTING.md` in
`D:\Projects\dawnfold\`) and referenced from `dawnfold`'s own `PRIVACY_POLICY.md`. **Changing or moving
this content affects Play Store compliance** — dawnfold's store listing points at this exact URL, so
don't rename/relocate the repo or change the deployed path without also updating the Play Console listing
and `dawnfold/STORE_LISTING.md`.
