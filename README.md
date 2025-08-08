# Tokyo Metropolitan University (TMU) Academic Poster Template

A professional LaTeX poster template designed for academic presentations at Tokyo Metropolitan University, specifically formatted for A1 size poster presentations commonly used in end-term semester presentations and research conferences.

## Overview

This template uses the `baposter` document class to create visually appealing academic posters suitable for:
- End-term semester presentations at Tokyo Metropolitan University
- Research conferences and symposiums
- Graduate student poster sessions
- Academic research showcases

## Template Specifications

- **Paper Size**: A1 (594mm × 841mm)
- **Orientation**: Portrait
- **Document Class**: baposter with 0.5 font scale
- **Color Scheme**: Professional blue and green CMYK colors
- **Layout**: Multi-column header box structure

## Quick Start

### Prerequisites

Ensure you have a LaTeX distribution installed with the following packages:
- `baposter` document class
- `wrapfig`, `lmodern`, `xcolor`, `amsmath`, `amssymb`, `multicol`, `adjustbox`
- PDF compilation support (`pdflatex`)

### Compilation

```bash
# Basic compilation
pdflatex poster.tex

# Full compilation with bibliography
pdflatex poster.tex
bibtex poster
pdflatex poster.tex
pdflatex poster.tex

# Using latexmk (if available)
latexmk -pdf poster.tex
```

### Cleaning Build Files

```bash
# Remove auxiliary files
rm -f *.aux *.bbl *.blg *.fdb_latexmk *.fls *.log *.synctex.gz

# Keep only essential files
ls *.tex *.cls *.bib figures/ poster.pdf
```

## Project Structure

```
├── poster.tex           # Main LaTeX document
├── baposter.cls         # Custom document class
├── figures/             # All poster figures and images
│   ├── *.pdf           # Research plots and charts
│   ├── *.png           # Images and photos
│   └── university_logo.png
├── poster.bib          # Primary bibliography file
├── references.bib      # Additional references
├── poster-blx.bib      # Bibliography LaTeX file
└── poster.pdf          # Final compiled poster
```

## Template Features

### Visual Design
- **Professional Color Scheme**: Custom CMYK colors (darkblue, lightblue, darkgreen, lightgreen)
- **Clean Layout**: Organized header boxes with proper spacing
- **Typography**: Latin Modern font with Unicode support
- **Graphics Integration**: Automatic figure path management

### Content Organization
- **Multi-column layouts** for efficient space utilization
- **Header box system** for structured content sections
- **Custom environments**:
  - `boenumerate`: Bold numbered lists
  - `compresslist`: Compact spacing for lists
- **Flexible positioning** of content blocks

### Academic Features
- **Bibliography support** with multiple `.bib` files
- **Mathematical notation** support (amsmath, amssymb)
- **Figure management** with centralized `figures/` directory
- **Professional formatting** suitable for academic standards

## Customization Guide

### Colors
Modify the color definitions in `poster.tex`:
```latex
\definecolor{darkgreen}{cmyk}{0.8,0,0.8,0.45}
\definecolor{lightgreen}{cmyk}{0.8,0,0.8,0.25}
\definecolor{darkblue}{cmyk}{1,0.5,0,0.3}
\definecolor{lightblue}{cmyk}{0.5,0.25,0,0.1}
```

### Layout
The poster uses a header box system. Each section is defined as:
```latex
\headerbox{Title}{name=sectionname,column=0,row=0}{
    % Content here
}
```

### Figures
Place all images in the `figures/` directory. Reference them directly:
```latex
\includegraphics[width=\textwidth]{filename.pdf}
```

## Tokyo Metropolitan University Guidelines

This template is designed to meet common academic poster presentation standards at TMU:

- **A1 Size**: Standard for university poster sessions
- **Professional Appearance**: Suitable for graduate presentations
- **Research Focus**: Optimized for technical and scientific content
- **Conference Ready**: Appropriate for academic symposiums

### Typical Use Cases at TMU
- Graduate school research presentations
- End-term semester poster sessions
- Department poster competitions
- Research center presentations
- Conference poster submissions

## Bibliography Management

The template supports multiple bibliography files:
- `poster.bib`: Primary references
- `poster-blx.bib`: Auto-generated bibliography file

Add references in standard BibTeX format and cite using `\cite{key}`.

## Tips for Success

1. **Content Balance**: Use the multi-column layout effectively
2. **Visual Hierarchy**: Leverage the color scheme for emphasis
3. **Figure Quality**: Ensure all figures are high-resolution
4. **Text Size**: The 0.5 font scale is optimized for A1 viewing distance
5. **Consistent Styling**: Follow the established formatting patterns

## Support and Troubleshooting

### Common Issues
- **Compilation Errors**: Ensure all required packages are installed
- **Figure Problems**: Check that all images exist in `figures/` directory
- **Bibliography Issues**: Run the full compilation sequence with bibtex

### Getting Help
- Check the LaTeX compilation log for specific error messages
- Ensure your LaTeX distribution includes the baposter class
- Verify all image files are accessible and properly formatted

---

**Note**: This template has been used successfully for research presentations on "Learning Robust Bipedal Locomotion Across Variable Farm Soil Structures via Multistages Deep Reinforcement Learning" and other technical research projects at TMU.