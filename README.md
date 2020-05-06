# An Example of Documentation by LuaLaTeX with VSCode

An example of documentation by LuaLaTeX with VSCode.

This example will produce [prj/out/main.pdf](prj/out/main.pdf) after saving [prj/main.tex](prj/main.tex).

## Environment

- Windows 10 Pro 10.0.18363 build 18363
- TeX Live 2020/W32Tex
- Visual Studio Code 1.44.2 (March 2020 release)
  - LaTeX Workshop 8.9.0

## Expected Workflow

1. Add/modify TeX files.
1. Auto Build on Save (by latexmk with LuaLaTeX and biber).
1. View LaTeX PDF file by Ctrl+Alt+V.
    - Jump by SyncTeX. (PDF → TeX: Ctrl+Click, TeX → PDF: Ctrl+Alt+J)

## Features of Example

- For easy documentation in Japanese. we set "\documentclass[lualatex,ja=standard]{bxjsarticle}" (see [preamble.tex](prj/preamble.tex)).
- usepackage [subfiles](https://ctan.org/pkg/subfiles) for partial build.
  - If you save [prj/refer/main.tex](prj/refer/main.tex), you will get [prj/refer/out/main.pdf](prj/refer/out/main.pdf), for example.
  - The output dir "out" is specified by "latex-workshop.latex.outDir" at [.vscode/settings.json](.vscode/settings.json). This may change relative path to master in "\documentclass[/path/to/master.tex]{subfiles}"
- usepackage [BibLaTeX](https://www.ctan.org/pkg/biblatex) for single bib file.
