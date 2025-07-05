# jottr — Product Roadmap

`jottr` is a lightweight, developer-first scratchpad designed for quick thinking, note-taking, and text manipulation. It's not a Markdown editor, a to-do manager, or a collaborative notes app — it’s a fast, keyboard-friendly space to **jot, edit, and move on.**

This roadmap outlines the pre-MVP and post-MVP development phases to guide contributors and collaborators.

---

## 📦 Tech Philosophy

* **Cross-platform:** Built with Tauri for eventual portability (Mac first).
* **FS-native:** All notes are stored as flat files on the filesystem.
* **Lightweight metadata only:** SQLite (or similar) may be used for optional tagging, indexing, and expiry tracking — but never as the source of truth.

---

## ✅ MVP Roadmap (Mac-Only First Release)

### 🔹 Phase 1: Core Editor (Plain Text)

* Create, rename, delete notes
* Autosave to filesystem
* Show files in sidebar
* Simple folder-based hierarchy
* Open file in Monaco Editor pane
*  Cmd+N for new note

### 🔹 Phase 2: Polish and Usability

* Toggle dark/light theme
* Restore open tabs/layout on restart
* Search/switch notes with Cmd+P
* CLI shortcut to open jottr directly
* Multi-cursor, Option+Drag, easy duplicate, select all occurrence & other text manipulation shortcuts

---

## 🚀 Post-MVP Features

### 🔧 Formatter Module (Modular)

* Optional plugins: JSON, YAML, SQL, etc.
* Trigger with Cmd+Shift+F or command palette
* Configurable per file type, ask file type if this module is enabled

### 🔁 Diff Checker

* Compare two notes side-by-side
* Inline or split view
* Launch from file list or open tabs

### 🔍 Tagging & Fuzzy Search

* Add `#tags` in sidebar or content
* Fuzzy search by title, tag, or content
* Filters by tag or recency

### 🧼 Cleanup Features

* Auto-expire old, unopened notes
* Trash view with restore
* “Smart Clean” for low-use notes (preview + delete)

### 🎛️ Power Features

* Custom keymap / import presets
* Cmd+K command palette
* jottr starts at login & Cmd+J to open jottr from anywhere

---

## 🛑 Explicit Non-Goals

### 🚫 Cloud Sync

This is a **local-only** tool. Notes are yours and live on your machine. We will not build sync, backups, or accounts.

### 🚫 Runtime Environment

This is **not a dev runner**. You cannot apply YAMLs, execute HTML, or run scripts inside jottr. It is a thought scratchpad, not an IDE or rendering tool.

### 🚫 Markdown or Rich Formatting

Plaintext only. Formatters may exist (for structure), but we do not support WYSIWYG, Markdown preview, or block-style editors.

---

## 🤝 Want to Contribute?

* Clone the repo, run locally, suggest small self-contained improvements.
* All discussions, suggestions, and PRs should respect the simplicity-first, filesystem-native philosophy.

We want `jottr` to be the **fastest way for developers to think on text** — no distractions, no bloat.

> "It’s not for publishing. It’s for clarity while you think."

---

## 💬 Your Feedback is Valuable

Does a tool like this make your life easier? Does something like this already exist for you?

What would make `jottr` better — *keeping in mind* its commitment to simplicity, intuitiveness, and its core focus: helping developers quickly jot down unstructured or transient thoughts?

We believe most tools either:

* Focus solely on structured note-taking (like Obsidian, Bear, or Notion)
* Or are full-blown IDEs with heavy workflows

`jottr` lives in between — it’s a place to **think in plaintext, manipulate fast, and move on.**

---

## 📌 Sample Use Cases

Here are some real-world scenarios where `jottr` makes things easy:

* **Quickly check the difference between two JSONs** — open both, hit Cmd+Shift+D.
* **Copy multiple lines and wrap each in quotes**, or append commas — fast multiline editing like a pro.
* **Format messy SQL** just to make sense of it — no copy-pasting to a formatter website.
* **Copy-paste a config or JSON snippet**, tweak a few lines, save it for reference.
* **Draft a config or command**, fiddle until it's perfect, then move it elsewhere.
* **Jot down a one-liner shell command** you just discovered before you forget it.
* \*\*Write a quick SOP\*\* you’ll paste to Slack or Confluence later.
* **Capture rough points during a call or meeting** that you'll polish later.
* **Write a message, note, or list to draft** before moving it to email, chat, or anywhere else.

If it lives in plaintext and helps you think — `jottr` is the right space for it.
