<h1 align="center">NovaBeamer Theme</h1>

<h3 align="center">A clean LaTeX Beamer theme for academic and scientific presentations.</h3>

<p align="center">
  <a href="https://ctan.org/pkg/novabeamer-theme">
    <img src="https://img.shields.io/ctan/v/novabeamer-theme?label=CTAN&color=red">
  </a>
  <a href="./LICENSE">
    <img src="https://img.shields.io/badge/license-LPPL%201.3c-blue">
  </a>
  <img src="https://img.shields.io/badge/LaTeX-Beamer-blue">
  <img src="https://img.shields.io/badge/contributions-welcome-orange">
  <a href="https://github.com/Riccardo-Martelli/NovaBeamer-Theme/stargazers">
    <img src="https://img.shields.io/github/stars/Riccardo-Martelli/NovaBeamer-Theme">
  </a>
  <a href="https://github.com/Riccardo-Martelli/NovaBeamer-Theme/network/members">
    <img src="https://img.shields.io/github/forks/Riccardo-Martelli/NovaBeamer-Theme">
  </a>
</p>

<img src="media/divider.svg" width="100%" height="4">

<p align="center">
  <img src="media/preview-title.png" width="45%" alt="NovaBeamer title page">
  <img src="media/preview-blocks.png" width="45%" alt="NovaBeamer frame with blocks">
</p>

* **Standard Beamer integration:** loads with the native `\usetheme` command.
* **Customizable colors:** one theme color, redefinable in your preamble to match your institution.
* **Clean layout:** rounded title boxes, full-width frame titles and a minimal footline with author, title, date and frame number.
* **Title page:** title and subtitle in a colored box, with support for `\titlegraphic`.

<img src="media/divider.svg" width="100%" height="4">

## Contents

* [Requirements](#requirements)
* [Compatibility](#compatibility)
* [Installation](#installation)
* [Usage](#usage)
  * [Version 1.0 and Overleaf](#version-10-and-overleaf)
* [Customization](#customization)
* [Example and documentation](#example-and-documentation)
* [Changelog](#changelog)
* [Maintainer](#maintainer)
* [License](#license)

<img src="media/divider.svg" width="100%" height="4">

## Requirements

* A LaTeX distribution with the `beamer` class
* The `tikz` and `comment` packages (loaded by the theme)
* A LaTeX kernel from October 2020 or later

<img src="media/divider.svg" width="100%" height="4">

## Compatibility

| Distribution | Status |
|---|---|
| TeX Live | included as `novabeamer-theme` |
| MiKTeX | included as `novabeamer-theme` |
| Overleaf | included through TeX Live; as of November 2026 it ships version 1.0, see [Version 1.0 and Overleaf](#version-10-and-overleaf) |
| Local copy | put `beamerthemenovabeamer.sty` next to your `.tex` file |

<img src="media/divider.svg" width="100%" height="4">

## Installation

The theme is part of TeX Live and MiKTeX, so an up to date distribution already has it. To use the version in this repository instead:

```bash
git clone https://github.com/Riccardo-Martelli/NovaBeamer-Theme.git
```

Then either copy `beamerthemenovabeamer.sty` into the folder of your presentation, or place it in your local TeX tree and refresh the filename database:

```bash
texhash
```

<img src="media/divider.svg" width="100%" height="4">

## Usage

```latex
\documentclass{beamer}
\usetheme{novabeamer}

\title{Sample Presentation}
\author{Your Name}
\institute{Your Institution}
\date{\today}

\begin{document}

\frame{\titlepage}

\begin{frame}{Introduction}
Welcome to this presentation using the NovaBeamer Theme.
\end{frame}

\end{document}
```

### Version 1.0 and Overleaf

Version 1.0 shipped the file as `novabeamer.sty`, loaded with `\usepackage{novabeamer}`. Version 1.1 renamed it to `beamerthemenovabeamer.sty` so that `\usetheme` works. If your distribution still provides version 1.0 (Overleaf did as of November 2026), use `\usepackage{novabeamer}`, or load whichever file is available:

```latex
\IfFileExists{beamerthemenovabeamer.sty}{\usetheme{novabeamer}}{\usepackage{novabeamer}}
```

<img src="media/divider.svg" width="100%" height="4">

## Customization

The theme color is `sithred`. Redefine it after `\usetheme` to change the title box, the section frames and the frame titles at once:

```latex
\usetheme{novabeamer}
\definecolor{sithred}{RGB}{0,70,140}
```

Frame titles and the footline are standard Beamer templates, so `\setbeamertemplate` and `\setbeamercolor` override them as usual.

<img src="media/divider.svg" width="100%" height="4">

## Example and documentation

* `examples/novabeamer-example.tex`: a full presentation with sections, blocks, columns, a table, a theorem, a figure and a bibliography. Compile it from the repository root, with a `bibtex` pass for the references.
* `doc/novabeamer-doc.pdf`: installation, usage and customization guide.

<img src="media/divider.svg" width="100%" height="4">

## Changelog

* **1.1**: renamed the main file to `beamerthemenovabeamer.sty` to support the standard `\usetheme` mechanism.
* **1.0**: first release on CTAN (Comprehensive TeX Archive Network), April 2025.

<img src="media/divider.svg" width="100%" height="4">

## Maintainer

<a href="https://github.com/Riccardo-Martelli">
  <img src="https://github.com/Riccardo-Martelli.png" width="90" alt="Riccardo Martelli">
</a>

**Riccardo Martelli**: [GitHub](https://github.com/Riccardo-Martelli) | [LinkedIn](https://www.linkedin.com/in/riccardomartelli/) | [Webpage](https://riccardo-martelli.github.io/.github.io/index.html) | [CTAN](https://ctan.org/pkg/novabeamer-theme)

<img src="media/divider.svg" width="100%" height="4">

## License

This work is released under the LaTeX Project Public License (LPPL) 1.3c. [View License](LICENSE)
