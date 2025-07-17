# University of Magallanes Thesis R Markdown Template

A comprehensive R Markdown template for Honours, Master's, and PhD theses at the University of Magallanes, specifically designed for the Antarctic and SubAntarctic Science doctoral program.

## Overview

This repository provides a complete thesis template using R Markdown with the `bookdown` package. The template is adapted from the [unofficial University of Toronto R Markdown thesis template](https://www.sgs.utoronto.ca/academic-progress/program-completion/formatting/) developed by Francois Pitt, and has been customized for the University of Magallanes requirements.

## Key Features

- **Institutional Customization**: Tailored for University of Magallanes branding and formatting requirements
- **Flexible Metadata**: Customizable school/department, university, country, and logo through YAML configuration
- **Academic Structure**: Support for director and co-directors (thesis supervisors)
- **Multi-format Output**: Primary focus on PDF generation with LaTeX backend
- **Chapter Management**: Support for both R Markdown and LaTeX chapters
- **Reproducible Research**: Integrated code execution and dynamic document generation

## Differences from Toronto Template

While largely based on the Toronto template, this version includes:

- University of Magallanes-specific formatting and styling
- Customizable institutional metadata (school, department, country, logo)
- Enhanced PDF metadata fields (subject and keywords)
- Support for thesis director and co-directors
- Adapted citation and bibliography styles for Antarctic research

## Requirements

### Essential Software

1. **R and RStudio**
   - Download R from [CRAN](https://cran.r-project.org/)
   - Download RStudio from [RStudio website](https://www.rstudio.com/)

2. **Required R Packages**
   ```r
   install.packages('bookdown')
   install.packages('knitr')
   install.packages('rmarkdown')
   ```

3. **LaTeX Distribution**
   
   **Option 1: TinyTeX (Recommended)**
   ```r
   install.packages('tinytex')
   tinytex::install_tinytex()
   ```
   
   **Option 2: Full LaTeX Installation**
   - Download from [LaTeX Project](https://www.latex-project.org/get/)
   - Choose appropriate distribution for your OS (TeX Live, MiKTeX, etc.)

### Recommended Tools

- **RStudio**: Primary IDE for R Markdown development
- **Sublime Text**: Alternative text editor for advanced users
- **Git**: Version control (recommended for thesis management)

## Quick Start

1. **Clone or Download the Repository**
   ```bash
   git clone https://github.com/MauroMardones/myThesis.git
   cd myThesis
   ```

2. **Open in RStudio**
   - Open `myThesis.Rproj` in RStudio
   - This will set up the proper working directory and project settings

3. **Compile the Thesis**
   ```r
   bookdown::render_book("index.Rmd", "bookdown::pdf_book")
   ```

4. **Preview Output**
   - The compiled PDF will be generated in the `_book/` directory
   - Open `_book/thesis.pdf` to view the result

## Project Structure

```
myThesis/
├── index.Rmd              # Main configuration 
├── _bookdown.yml          # Bookdown configuration
├── myThesis.Rproj         # RStudio project file
├── ut-thesis.cls          # LaTeX class file
├── ut-thesis.tex          # LaTeX template
├── chapters/              # Individual chapter files
│   ├── 01-intro.Rmd
│   ├── 02-chap2.Rmd
│   ├── 03-chap3.Rmd
│   └── ...
├── figures/               # Image files
├── bib/                   # .bib folder
│   ├── ThesisDOCAS.bib    # Bibliography file
└── _book/                 # Compiled output (generated)
```

## Customization

### Basic Configuration

Edit the YAML header in `index.Rmd`:

```yaml
---
title: "Your Thesis Title"
author: "Your Name"
date: "Submission Date"
university: "University of Magallanes"
school: "Graduate School"
department: "Antarctic and SubAntarctic Science Program"
director: "Dr. Director Name"
codirector: "Dr. Co-director Name"
country: "Chile"
logo: "path/to/logo.png"
keywords: "Antarctic, marine ecology, krill"
subject: "Antarctic Science"
---
```

### Advanced Customization

- **LaTeX Styling**: Modify `ut-thesis.cls` and `ut-thesis.tex`
- **Chapter Organization**: Edit `_bookdown.yml` to add/remove chapters
- **Output Formats**: Adjust `_output.yml` for different output options
- **Bibliography**: Update `references.bib` with your citations

## Writing Your Thesis

### Adding Chapters

1. Create new `.Rmd` files in the root directory
2. Name them with number prefixes (e.g., `03-methods.Rmd`)
3. Update `_bookdown.yml` to include new chapters

### Including Figures and Tables

```r
# For figures
knitr::include_graphics("figures/my-figure.png")

# For tables
knitr::kable(my_data, caption = "My Table")
```

### Citations and References

Use standard R Markdown citation syntax:
```markdown
[@author2023] or @author2023
```

## Troubleshooting

### Common Issues

1. **LaTeX Errors**: Ensure all required LaTeX packages are installed
2. **Package Dependencies**: Run `install.packages()` for missing packages
3. **File Paths**: Use relative paths for figures and data files
4. **Encoding Issues**: Ensure all files are saved in UTF-8 encoding

### Getting Help

- Check the [bookdown documentation](https://bookdown.org/yihui/bookdown/)
- Review R Markdown [cheat sheets](https://www.rstudio.com/resources/cheatsheets/)
- Open issues on the [GitHub repository](https://github.com/MauroMardones/myThesis/issues)

## Contributing

Contributions to improve this template are welcome! Please:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

This template is provided under the same license as the original Toronto template. Please check the repository for specific licensing information.

## Acknowledgments

- Original template by Francois Pitt (University of Toronto)
- Adapted for University of Magallanes by Mauricio Mardones
- Antarctic and SubAntarctic Science Doctoral Program, University of Magallanes

## Repository

🔗 **GitHub Repository**: [https://github.com/MauroMardones/myThesis](https://github.com/MauroMardones/myThesis)

---

*For questions specific to the University of Magallanes requirements or Antarctic research formatting, please contact the doctoral program coordinators.*
