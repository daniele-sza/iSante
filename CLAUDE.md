# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Context

This repository holds both the public one-page website for **Instituto Isanté / Grupo Silvestre Santé** (`index.html`, deployed via GitHub Pages — see `.github/workflows/deploy.yml`) and the institutional source documents (Portuguese PDFs and Word files) behind its content.

## Folder Structure

- `index.html` — the single-page site. Sections are `<section id="s0">`…`<section id="s9">`, matching the nav order: Home, Quem Somos, Nosso Ecossistema, Linha do Tempo, Ciência, Portfólio, Congresso 2026, Cooperação, Parceiros, Contato.
- `assets/` — every image/PDF the site actually references, mirrored to that section order:
  - `assets/geral/` — shared logos used in header/footer across all sections.
  - `assets/00-home/`, `assets/02-ecossistema/`, `assets/03-linha-do-tempo/`, `assets/05-portfolio/pdf/`, `assets/06-congresso-2026/` (+ `documentos/` for the non-linked congress `.pptx`), `assets/08-parceiros/`, `assets/09-contato/` — one folder per section, containing only what that section uses. Sections with no unique media (Quem Somos, Ciência, Cooperação) have no folder.
  - `assets/nao-utilizadas/` — images not referenced by `index.html` (raw/unedited photo originals in `originais-sem-otimizacao/`, miscellaneous unused photos in `fotos-diversas/`). Kept for reference, not linked anywhere.
- `documentos/` (formerly `CLODE/`) — institutional source documents, organized by category:

| Folder | File | Purpose |
|--------|------|---------|
| `projetos/` | `Projeto_Amazonia_Sem_Fronteiras_24_meses_FINAL_04062026.pdf` | Final version of the "Amazônia Sem Fronteiras" 24-month project (finalized 2026-06-04). Distinct from the larger `assets/05-portfolio/pdf/Amazonia.pdf` linked on the site's Portfólio card. |
| `portfolio-investimentos/` | `Portfolio de Investimentos em Projetos Silvestre Sante.docx` | Investment portfolio across Silvestre Santé projects |
| `linha-do-tempo/` | `Linha do Tempo Ações Sociais Silvestre Sante.docx` | Timeline of social actions by Silvestre Santé |
| `publicacoes-cientificas/` | `Publicações e Linha do Tempo Cientifica Grupo Silvestre Santé.docx` (+ a `(1)` duplicate) | Scientific publications and research timeline |
| `estudos-clinicos/` | `Quadro_Estudos_Clinicos.docx` | Clinical studies overview |
| `contribuicoes-site/` | `CONTRIBUIÇOES PARA O SITE DO ISANTE .docx` | Raw content contributions for the site copy |

## Working with These Documents

- PDF files cannot be read with the standard `Read` tool unless `pdftoppm` is installed. Use the user's own document tooling or request content be pasted in.
- Word (`.docx`) files can sometimes be read as raw XML; content may be partially legible via `Read`, though formatting will be stripped.
- All documents are in **Brazilian Portuguese** — respond in Portuguese when asked to draft, edit, or summarize content from them.
- When adding a new image/PDF used by `index.html`, put it under `assets/<section-folder>/` (create the section folder if it doesn't exist yet) and reference it with that relative path — do not recreate top-level `IMAGEM/` or `pdf/` folders.
