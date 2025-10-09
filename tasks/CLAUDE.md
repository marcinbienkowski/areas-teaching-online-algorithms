# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a LaTeX-based repository containing problem sets and solutions for online algorithms coursework. The repository is structured around individual problem sets (c1-c12) and additional materials in Polish.

## Build Commands

### Primary Build System
- `make all` - Compiles all PDF files from LaTeX sources
- `make <filename>.pdf` - Compiles a specific PDF (e.g., `make c1.pdf`)
- `make clean` - Removes auxiliary LaTeX files (.aux, .log, .synctex.gz, etc.)
- `make distclean` - Removes all generated files including PDFs

### LaTeX Compilation
The Makefile uses `pdflatex` with synctex enabled and runs compilation twice for proper cross-references:
```bash
pdflatex -synctex=1 <filename>.tex
pdflatex -synctex=1 <filename>.tex
```

## Architecture and Structure

### Main Directory
- **Problem sets**: `c1.tex` through `c12.tex` - Individual problem set files
- **EXTRA.tex**: Additional unused problems
- **macros.tex**: Shared LaTeX macros and styling for problem sets
- **Makefile**: Build configuration

### Solutions Directory (`rozwiazania/`)
- Contains solution files with different styling
- **macros.tex**: Separate macro file for solutions with different formatting
- **Solution files**: Individual `.tex` files for specific problems (e.g., `slack.tex`, `rand-mtf.tex`)
- **pict/**: Directory containing PDF figures for solutions

### LaTeX Structure
Both main and solutions directories use similar patterns:
- Document class: `article` with 11pt font on A4 paper
- Modern packages: amsmath, amsfonts, xcolor, microtype, enumitem, geometry
- Custom macros for algorithm notation (`\ALG`, `\OPT`, `\CNT`, etc.)
- Modern styling with improved typography and professional layout

#### Modern Styling Features
- **Typography**: 
  - Latin Modern fonts as base (can be overridden with pxfonts for Palatino)
  - microtype for improved text rendering
  - 1.05 line spacing for better readability
  - T1 font encoding for Polish language support
  
- **Layout and Margins**:
  - Margins: 2.5cm left/right, 2cm top/bottom for optimal readability
  - Empty page style (no headers/footers)
  - Professional spacing with colored elements
  
- **Color scheme**: 
  - Primary blue: RGB(0,102,153) for headers and important elements
  - Accent gray: RGB(85,85,85) for secondary elements
  
- **Task formatting**: 
  - Description lists with colored task labels ending in periods (e.g., "Zadanie 1.")
  - Bold blue point values (e.g., "(1 pkt.)")
  - Enumerate lists with colored a), b), c) labels
  - Consistent spacing and professional appearance

#### Algorithm Notation
- `\ALG` - Algorithm in small caps
- `\OPT` - Optimal algorithm in small caps  
- `\DET` - Deterministic algorithm
- `\RAND` - Randomized algorithm
- `\CNT`, `\CONT` - Specific algorithm names
- `\E` - Expectation symbol
- All algorithm names use `\textsc{}` for small caps styling

### File Dependencies
- All `.tex` files depend on their respective `macros.tex`
- PDF generation requires two pdflatex passes for proper references
- Solutions use a more elaborate macro system with theorem environments

## Development Workflow

When working with this repository:
1. Edit `.tex` files for content changes
2. Update `macros.tex` for shared styling/commands
3. Use `make` to build PDFs
4. Use `make clean` before committing to remove auxiliary files

## Recent Updates

The repository has been modernized with:
- Professional typography and color scheme
- Consistent task numbering with periods (Zadanie 1., Zadanie 2., etc.)
- Modern LaTeX packages for improved rendering
- Optimized margins for academic documents
- Small caps styling for algorithm names

The repository follows Polish academic conventions and contains coursework on competitive online algorithms including topics like cow searching, ski rental, caching, load balancing, and other online optimization problems.