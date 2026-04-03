# 🔀 curl Comparator & curl Diff — Compare Two curl Commands Online (HTTP Request Diff)

[![Open tool](https://img.shields.io/badge/Open-curl%20compare-6366f1?style=for-the-badge&logo=googlechrome&logoColor=white)](https://spoold.com/tools/http/curl/compare)
[![Site](https://img.shields.io/badge/spoold.com-live-22c55e?style=flat-square&logo=googlechrome&logoColor=white)](https://spoold.com/tools/http/curl/compare)
![Client-side](https://img.shields.io/badge/processing-client--side-0ea5e9?style=flat-square&logo=javascript&logoColor=white)
![No sign-up](https://img.shields.io/badge/sign--up-not%20required-64748b?style=flat-square)
[![Source](https://img.shields.io/badge/code-open%20source-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/thespoold/spoold)

[![Next.js](https://img.shields.io/badge/Next.js-16-000000?style=flat-square&logo=nextdotjs&logoColor=white)](https://nextjs.org)

**Free browser-based curl comparator and curl comparison tool.** Paste **two curl commands** side by side and see a **structured diff** of **HTTP method**, **URL** (base + **query parameters**), **headers**, **auth**, **cookies**, **body**, and common **flags**—plus a **Monaco** side-by-side diff and a **raw line diff** when parsing is partial or you need the full command text. Same **curl parser** as Spoold’s **curl → code** converter. **Nothing is uploaded**; comparison runs **client-side**.

**Live tool:** [spoold.com/tools/http/curl/compare](https://spoold.com/tools/http/curl/compare)

---

## 📑 Table of contents

- [What this tool is for](#what-this-tool-is-for)
- [Who searches for this (keywords)](#who-searches-for-this-keywords)
- [Features](#features)
- [How to use](#how-to-use)
- [Local storage & history](#local-storage--history)
- [Parser & limits](#parser--limits)
- [Related tools](#related-tools)
- [Tech stack & privacy](#tech-stack--privacy)
- [Repository](#repository)

---

## 🎯 What this tool is for

Use this **online curl diff** when you need to:

- **Compare curl commands** from docs vs DevTools, **staging vs production**, or two API versions without eyeballing long one-liners.
- **Spot differences** in **Authorization**, **query strings**, **headers**, **JSON bodies** (pretty-printed line diff when both bodies parse as JSON), and **curl flags** (`-L`, `-k`, `--compressed`, etc.).
- **Debug HTTP requests** as text: see **what changed** in both **structured tables** and a **full raw diff**.
- **Iterate quickly** with **swap**, **samples**, **clear**, and optional **document history** in the app.

It is part of **[Spoold](https://spoold.com)** — developer utilities in the browser.

---

## 🔎 Who searches for this (keywords)

This README and the live page target searches such as:

**Core intent:** `curl comparator`, `curl comparison tool`, `curl command comparator`, `curl compare`, `curl compare online`, `compare curl commands`, `curl diff`, `diff curl requests`, `two curl commands`, `side by side curl`

**HTTP / API:** `http request compare`, `compare http requests`, `curl request diff`, `api request diff`, `diff curl`, `compare curl`

---

## ✨ Features

| Area | What you get |
|------|----------------|
| **Dual editor** | Monaco **DiffEditor** (shell) for **curl A** vs **curl B**; edit and paste on both sides. |
| **Structured comparison** | When both sides parse: **method**, **URL** split into **base** and **query** (when the URL is valid), **headers** (union of keys), **body** diff (JSON-pretty when possible), **auth**, **cookies**, **follow / insecure / compressed** flags. |
| **Single curl mode** | If only one pane has a valid curl, a **summary** still shows parsed fields; add a second command to diff. |
| **Raw diff** | **Line-based diff** of the full command text—useful for odd flags or when structured parsing is incomplete. |
| **Shared parser** | Same **`parseCurl`** pipeline as **[curl → code](https://spoold.com/tools/http/curl)** for consistent behavior. |
| **Samples & swap** | **Both samples** loads example curls; **Swap** exchanges A/B; **Clear A/B** resets panes. |
| **History** | **History** panel for recent documents (IndexedDB-backed flow consistent with other Spoold tools). |
| **Handoff** | Compatible with Spoold **Magic Box** / `#data=` style landing so the left command can be **pre-filled** from detection (see in-app guide). |

---

## 👣 How to use

1. Open **[curl compare](https://spoold.com/tools/http/curl/compare)**.
2. Paste **curl A** (original) and **curl B** (modified) into the diff editor, or try **Both samples**.
3. Read **Structured comparison** for method, URL, query, headers, body, auth, and cookies.
4. Use the **raw** section when you need **full-command** differences or the parser skipped a niche flag.
5. Optionally open **History** to reload recent work.

---

## 💾 Local storage & history

The UI may persist editor content using **local stash keys** such as `spoold-curl-compare-a` and `spoold-curl-compare-b` (session continuity in the browser). **History** uses Spoold’s **document storage** (e.g. IndexedDB) so you can return to recent comparisons—still **on your device**, not sent to Spoold as “curl comparison as a service.”

---

## ⚙️ Parser & limits

- Covers **common curl flags** used in typical API calls (`-X`, `-H`, `-d`, `-u`, `-b`, `-L`, `-k`, `--compressed`, and more—see the in-page **Guide** for nuance).
- **Does not** execute requests or validate against a live server—this is a **text and structural** diff only.
- If one or both commands **fail to parse**, you still get **parse errors** per side (when applicable) and the **raw line diff** of the full strings.

---

## 🔗 Related tools

- **[curl → code](https://spoold.com/tools/http/curl)** — Convert a **single** curl to fetch, Axios, Python, etc.
- **[Text Diff](https://spoold.com/tools/text/diff)** — Generic two-text compare.
- **[URL inspect](https://spoold.com/tools/url/inspect)** — Break down URLs and parameters.

---

## 🛠️ Tech stack & privacy

- Built with **Next.js** (React) and **Monaco Editor** (`DiffEditor`).
- Uses **`diff`** for line diffs and shared **curl parsing** utilities under `src/lib/`.
- **No server-side curl execution** in this tool: your commands stay in the **browser** unless you choose a separate Spoold share/cloud flow that applies to other tools.

---

## 🐙 Repository

Spoold: **[github.com/thespoold/spoold](https://github.com/thespoold/spoold)** — clone, `pnpm install`, `pnpm dev`, then open `/tools/http/curl/compare`.

---

**Spoold** — *Paste. Detect. Do.* · [spoold.com](https://spoold.com)
