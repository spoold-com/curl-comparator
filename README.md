# 🔀 curl Comparator — Compare Two curl Commands Online (curl diff)

[![Open tool](https://img.shields.io/badge/Open-curl%20compare-6366f1?style=for-the-badge&logo=googlechrome&logoColor=white)](https://spoold.com/tools/http/curl/compare)
[![Site](https://img.shields.io/badge/spoold.com-live-22c55e?style=flat-square&logo=googlechrome&logoColor=white)](https://spoold.com/tools/http/curl/compare)
![Client-side](https://img.shields.io/badge/processing-client--side-0ea5e9?style=flat-square&logo=javascript&logoColor=white)
![No sign-up](https://img.shields.io/badge/sign--up-not%20required-64748b?style=flat-square)
[![Source](https://img.shields.io/badge/code-open%20source-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/thespoold/spoold)

[![Next.js](https://img.shields.io/badge/Next.js-16-000000?style=flat-square&logo=nextdotjs&logoColor=white)](https://nextjs.org)
[![React](https://img.shields.io/badge/React-19-61DAFB?style=flat-square&logo=react&logoColor=black)](https://react.dev)
[![Monaco](https://img.shields.io/badge/Monaco-DiffEditor-007ACC?style=flat-square&logo=visualstudiocode&logoColor=white)](https://microsoft.github.io/monaco-editor/)
[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)]()

**Free [curl comparator](https://spoold.com/tools/http/curl/compare)** and **curl comparison tool**: paste **two curl commands** and get a **structured diff** (HTTP method, URL + query, headers, auth, cookies, body, flags), a **Monaco** side-by-side diff, and a **raw line diff** if parsing is partial. Same **curl parser** as **[curl → code](https://spoold.com/tools/http/curl)**. Runs **client-side** in your browser — no upload for the core compare.

---

## 🔎 What people search for

**curl comparator**, **curl comparison tool**, **curl command comparator**, **curl compare**, **curl compare online**, **compare curl commands**, **curl diff**, **diff curl requests**, **two curl commands**, **side by side curl**, **http request compare**, **compare http requests**, **curl request diff**, **api request diff**.

---

## ✨ What it does

- 🖥️ **Dual editor** — Monaco DiffEditor for curl **A** vs **B** (edit/paste both sides).
- 📊 **Structured diff** — Method, URL (base + query), headers, body (JSON-pretty when possible), auth, cookies, common flags.
- 📜 **Raw diff** — Full command text when you need every flag or the parser skipped something.
- 🔗 **One parser** — Same `parseCurl` pipeline as the [curl → code](https://spoold.com/tools/http/curl) tool.
- 🔁 **Samples & swap** — Example curls, swap A/B, clear panes.
- 🕐 **History** — Recent docs via IndexedDB (on your device).
- ✨ **Magic Box / `#data=`** — Left pane can be pre-filled from Spoold detection (see in-app guide).

---

## 👣 Quick start

1. Open **https://spoold.com/tools/http/curl/compare**
2. Paste curl **A** and **B**, or use **Both samples**.
3. Read **Structured comparison**; use **raw** for full-line differences.
4. Optional: **History** for recent work.

---

## 🔒 Privacy & limits

- 🔐 **Local-first:** diff runs in the browser; core flow does not send your curls to a server.
- ⛔ **No HTTP execution** — this tool only compares text; it does not run requests against APIs.
- ⚠️ **Secrets:** redact tokens before sharing screens or links.
- 📋 **Parser:** supports common curl flags (`-X`, `-H`, `-d`, `-u`, `-b`, `-L`, `-k`, `--compressed`, …). Rare flags may only appear in the raw diff.

**Local stash keys:** `spoold-curl-compare-a`, `spoold-curl-compare-b`. History uses browser storage (e.g. IndexedDB).

---

## 🔗 Related Spoold tools

| Tool | URL |
|------|-----|
| curl → code | https://spoold.com/tools/http/curl |
| Text diff | https://spoold.com/tools/text/diff |
| URL inspect | https://spoold.com/tools/url/inspect |

---

## 🛠️ Run from source

```bash
git clone https://github.com/thespoold/spoold.git
cd spoold && pnpm install && pnpm dev
```

Open `/tools/http/curl/compare` locally.

---

**Spoold** — *Paste. Detect. Do.* · [spoold.com](https://spoold.com) · [github.com/thespoold/spoold](https://github.com/thespoold/spoold)
