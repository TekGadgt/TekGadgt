# GitHub Profile README Design

## Purpose

A GitHub profile README that serves as a "hire me" funnel landing page. Target audience: people arriving from the cssdaily.dev about page (or elsewhere) who want to understand who Ryan is and what he builds. Tone: confident and personable — not salesy, but not shy either. Targeting senior full-stack roles with a frontend lean.

## Structure

### 1. Header — One-Liner Intro

A single line: name + what he does + a hint of confidence.

> **Ryan McGovern** — Full-stack engineer building tools people actually use.

No emoji, no "passionate about," no multi-sentence bio. The projects below do the talking.

### 2. Tech Badges

A single row of shields.io badges for core technologies. Covers both personal project stack and career experience:

- React
- Vue
- TypeScript
- PHP
- Go
- Astro
- Tailwind CSS
- SQLite
- Docker

Badges use `flat` style with each technology's brand color.

### 3. Featured Projects

Two project highlight blocks. Each contains:

- **Project name** linked to the GitHub repo
- **One-line hook** — what it is, framed to impress
- **2-3 technical bullet points** — the most interesting implementation details
- **Live site link** where applicable

#### cssdaily.dev

Link: [github.com/TekGadgt/cssdaily.dev](https://github.com/TekGadgt/cssdaily.dev) | Live: [cssdaily.dev](https://cssdaily.dev)

A daily CSS challenge game with AI-generated puzzles and real-time pixel-accurate scoring.

- Claude generates daily challenges, Playwright renders targets, GitHub Actions deploys — fully automated pipeline
- Pixel-level visual diffing engine scores your CSS in real time as you type
- Built with Astro, React, CodeMirror, Tailwind

#### Conclave Chat

Link: [github.com/TekGadgt/Conclave-Chat](https://github.com/TekGadgt/Conclave-Chat) | Live: [conclave.lol](https://conclave.lol)

A lightweight, self-hosted Discord alternative with text and voice chat.

- Full server/channel/message model with WebSocket real-time messaging
- Voice/video chat via LiveKit
- Ships as a single Go binary with the React frontend embedded
- Built with Go, React, TypeScript, SQLite, Docker

### 4. Social Links Footer

A clean row of plain text links separated by ` | `. No icons, no badges. The funnel is implicit — interesting projects lead to "who is this person?" lead to LinkedIn.

- [LinkedIn](https://www.linkedin.com/in/ryan-mcgovern-tekgadgt/)
- [Bluesky](https://bsky.app/profile/tekgadgt.dev)
- [tekgadgt.com](https://tekgadgt.com/)
- [cssdaily.dev](https://cssdaily.dev)
- [conclave.lol](https://conclave.lol)

## Technical Notes

- File: `README.md` in the TekGadgt/TekGadgt repo (GitHub profile repo)
- Pure Markdown — no HTML needed unless badge layout requires it
- Shields.io badges via `img.shields.io/badge/` URLs
- No GitHub stats widgets (stats and contribution graph are visible below the README on the profile page already)

## Out of Scope

- GitHub Actions or automation
- Dynamic content (pinned repos, auto-updating stats)
- Custom CSS/HTML beyond what GitHub Markdown supports
