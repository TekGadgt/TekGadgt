# GitHub Profile README Implementation Plan

> **For agentic workers:** REQUIRED: Use superpowers:subagent-driven-development (if subagents available) or superpowers:executing-plans to implement this plan. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build a GitHub profile README that serves as a confident, personable "hire me" funnel landing page.

**Architecture:** Single Markdown file with four sections: header, tech badges, featured projects, and social links. Uses shields.io for tech badges and standard GitHub-flavored Markdown throughout.

**Tech Stack:** Markdown, shields.io badges, HTML `<p align="center">` for badge centering (GitHub Markdown doesn't support centering natively)

**Spec:** `docs/superpowers/specs/2026-03-16-github-profile-readme-design.md`

---

## Chunk 1: Build the README

### Task 1: Write the header section

**Files:**
- Modify: `README.md`

- [ ] **Step 1: Replace the default README with the header**

Replace the entire contents of `README.md` (overwriting the default GitHub profile template) with:

```markdown
# Ryan McGovern

**Full-stack engineer building tools people actually use.**
```

Note: The spec describes a single-line format (`**Ryan McGovern** — Full-stack...`), but an H1 heading + bold subtitle renders significantly better on GitHub profile pages — the name gets proper visual weight as a page title. This is an intentional deviation.

- [ ] **Step 2: Commit**

```bash
git add README.md
git commit -m "feat: add profile README header"
```

---

### Task 2: Add tech badges

**Files:**
- Modify: `README.md`

- [ ] **Step 1: Add the badge row below the header**

Append below the header, after a blank line:

```html
<p align="center">
  <img alt="React" src="https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black" />
  <img alt="Vue" src="https://img.shields.io/badge/Vue-4FC08D?style=flat&logo=vuedotjs&logoColor=white" />
  <img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white" />
  <img alt="PHP" src="https://img.shields.io/badge/PHP-777BB4?style=flat&logo=php&logoColor=white" />
  <img alt="Go" src="https://img.shields.io/badge/Go-00ADD8?style=flat&logo=go&logoColor=white" />
  <img alt="Astro" src="https://img.shields.io/badge/Astro-BC52EE?style=flat&logo=astro&logoColor=white" />
  <img alt="Tailwind CSS" src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat&logo=tailwindcss&logoColor=white" />
  <img alt="SQLite" src="https://img.shields.io/badge/SQLite-003B57?style=flat&logo=sqlite&logoColor=white" />
  <img alt="Docker" src="https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white" />
</p>
```

Notes:
- Uses `flat` style per spec
- Each badge uses the technology's brand color
- HTML `<p align="center">` wrapper centers the badges and keeps them on one flowing line
- Logo slugs follow shields.io/simple-icons naming: `react`, `vuedotjs`, `typescript`, `php`, `go`, `astro`, `tailwindcss`, `sqlite`, `docker`

- [ ] **Step 2: Verify badges render correctly**

Open `https://github.com/TekGadgt` in a browser and confirm the badges display in a single row with correct logos and colors. (Or preview locally with a Markdown renderer that supports HTML.)

- [ ] **Step 3: Commit**

```bash
git add README.md
git commit -m "feat: add tech stack badges"
```

---

### Task 3: Add featured projects section

**Files:**
- Modify: `README.md`

- [ ] **Step 1: Add the two project blocks below the badges**

Append below the badge row, after a blank line:

```markdown
## Projects

### [cssdaily.dev](https://github.com/TekGadgt/cssdaily.dev)

A daily CSS challenge game with AI-generated puzzles and real-time pixel-accurate scoring. [Play it live](https://cssdaily.dev)

- Claude generates daily challenges, Playwright renders targets, GitHub Actions deploys — fully automated pipeline
- Pixel-level visual diffing engine scores your CSS in real time as you type
- Built with Astro, React, CodeMirror, Tailwind

### [Conclave Chat](https://github.com/TekGadgt/Conclave-Chat)

A lightweight, self-hosted Discord alternative with text and voice chat. [Try it live](https://conclave.lol)

- Full server/channel/message model with WebSocket real-time messaging
- Voice/video chat via LiveKit
- Ships as a single Go binary with the React frontend embedded
- Built with Go, React, TypeScript, SQLite, Docker
```

- [ ] **Step 2: Commit**

```bash
git add README.md
git commit -m "feat: add featured projects section"
```

---

### Task 4: Add social links footer

**Files:**
- Modify: `README.md`

- [ ] **Step 1: Add the social links row at the bottom**

Append at the end of the file, after a blank line and a horizontal rule:

```markdown
---

[LinkedIn](https://www.linkedin.com/in/ryan-mcgovern-tekgadgt/) | [Bluesky](https://bsky.app/profile/tekgadgt.dev) | [tekgadgt.com](https://tekgadgt.com/) | [cssdaily.dev](https://cssdaily.dev) | [conclave.lol](https://conclave.lol)
```

- [ ] **Step 2: Commit**

```bash
git add README.md
git commit -m "feat: add social links footer"
```

---

### Task 5: Final review

- [ ] **Step 1: Read the complete README and verify it matches the spec**

Check against `docs/superpowers/specs/2026-03-16-github-profile-readme-design.md`:
- Header: name + tagline, no emoji
- Badges: all 9 techs, `flat` style, brand colors
- Projects: both projects with repo links, live links, hooks, and bullet points
- Footer: 5 plain text links separated by `|`

- [ ] **Step 2: Push and verify on GitHub**

```bash
git push origin main
```

Open `https://github.com/TekGadgt` and confirm the profile README renders correctly.
