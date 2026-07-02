# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

This is **not a software project** — it is an **Obsidian vault** (personal knowledge-management / writing system). There is no build, test, or lint step. Content is Korean-language Markdown notes. The stated purpose (README) is a "failure log": recording the process, missteps, and rough thinking behind reading, writing, and tooling — the raw material for publishing (primarily Threads posts) and copywriting.

Work here means **reading, writing, organizing, and connecting Markdown notes**, respecting the folder pipeline and note conventions below.

## ⚠️ Required workflow — read before touching any file

- **Propose before acting.** Before creating, editing, or moving any file, present a plan (what file(s), what change, why) and get explicit approval. Do not act first and report after.
- **Never rewrite existing note content.** For files that already exist, the only permitted edits are: adding/updating YAML frontmatter, adding tags, and moving the file to a different folder. Do not alter the body text, headings, or wording of an existing note unless the user explicitly asks for a content edit.
- **Keep Korean filenames as-is.** Never rename, transliterate, or translate existing filenames when moving or editing a file.

## MOC (Map of Content) structure

This vault is organized around **MOC notes** — hub notes that index and link related notes by topic, acting as a navigable map rather than relying on folders alone. When organizing or connecting notes:

- Check whether a relevant MOC already exists before creating a new one; prefer adding a link to an existing MOC over creating a duplicate.
- A MOC note primarily consists of links (`[[note title]]`) to related notes, grouped under topic headings.
- New permanent/literature notes should be linked from an appropriate MOC when one exists, in addition to their direct wikilinks in `## 연결`.

## Folder pipeline (Zettelkasten / PARA-style)

The numeric prefixes encode a workflow, roughly inbox → refined → published. When creating or moving a note, place it by its stage, not just its topic:

- **`00.수집함`** — Inbox / fleeting collection. Unprocessed captures land here first.
- **`01.문헌메모`** — Literature notes. One note per idea distilled from a source (book, video, post), in the user's own words.
- **`02.영구메모`** — Permanent notes. Fully developed, self-standing ideas linked into the network.
- **`03.카피메모`** — Copywriting notes. Reverse-engineered analyses of hooks/headlines that worked, with a reusable formula (`## 공식`). Titles carry search keywords so patterns are findable later.
- **`04.리소스 모음`** — Resources (e.g. `References/` holds raw market-research clippings).
- **`99.보관함`** — Archive (inactive notes).
- **`998.템플릿`** — Templates (see below).
- **`999.파일보관함`** — Attachment / file storage.
- **`Excalidraw`** — Excalidraw drawings (`.md`-backed).

## Note conventions

- **Templates live in `998.템플릿`** and are the canonical structure for each note type. Match the corresponding template's frontmatter and headings when creating a note — do not invent a new layout:
  - `문헌메모 - 템플릿.md` → literature notes (frontmatter: `category`, `Date`, `출간연도`, `인물_저자`, `tags`, `출처`, `페이지`, `aliases`; sections: 한 줄 정의 / 핵심 / 내 사례·반례 / 출처 / 연결)
  - `영구 노트 - 템플릿.md`, `임시메모-템플릿.md` → 메모 / 생각(질문) / 원문(인용) / 출처(인물) / 연결(이유)
  - `콘텐츠 작업 메모 - 템플릿.md` → drafting pipeline: 발단 → 한 단계 더 → 날것 초안 → 헤드라인 설계 → 초안 → 발행 여부
  - `쓰레드 - 템플릿.md` → Threads post structure (multi-part with media)
  - `market-research 템플릿.md`
- **Frontmatter** commonly includes `date` (ISO, e.g. `2026-06-24T19:15:00`), `source`/`출처`, `tags`. Follow the surrounding notes' style rather than imposing a uniform schema.
- **Links** use Obsidian wikilinks `[[note title]]`. The `## 연결 (이유)` / `## 연결` section records *why* two notes connect, not just that they do. When adding a note, look for existing notes to link.
- **Voice**: notes are intentionally raw and first-person ("내 말로", "다듬지 말고"). Do not over-polish drafts into formal prose unless asked — the roughness is the point.
- **Filenames are the titles** (Korean, spaces allowed, no numeric IDs). Keep the search-keyword-forward naming, especially for `03.카피메모`.

## Git workflow

- Commit messages are terse, often a date (`2026.06.29 commit`) or short Korean note (`문헌 메모 추가`). Match this style; keep messages short and in Korean unless asked otherwise.
- There is **no `.gitignore`**, so `.obsidian/workspace.json` (Obsidian UI state) shows up as modified frequently. Treat these as noise — avoid committing workspace churn unless the user wants it, and don't stage everything blindly.
- `.trash/` holds Obsidian-deleted notes and may show as untracked; don't resurrect or commit it without being asked.

## Obsidian environment

- Community plugins in use: `obsidian-excalidraw-plugin`, `obsidian-style-settings`.
- The template folder is configured to `998.템플릿` in `.obsidian/templates.json`.
- Obsidian-specific skills are available (`obsidian:obsidian-markdown`, `obsidian:obsidian-cli`, `obsidian:json-canvas`, `obsidian:obsidian-bases`, `obsidian:defuddle`) — prefer these for wikilink/callout/frontmatter editing, Canvas files, and reading web sources into the vault.
