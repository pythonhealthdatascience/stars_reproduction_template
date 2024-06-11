<!-- TODO: Remove "[Template]" and amend to refer to the first author and year of the original study -->
# [Template] STARS: Computational reproducibility of [Author] et al. [Year]

<!-- TODO: Remove this paragraph -->
**This is a template repository for assessing the computational reproducibility of simulation studies on STARS. To use this template, please select the "use this template" button and then "create a new repository"**.

**If you are using VSCode and encounter an error rendering files containing code - e.g. "*ERROR: Not a directory (os error 20): stat '/bin/python3/'*" - this is likely because you haven't set an interpreter for that file. You can do so via Ctrl+Shift+P "Python: Select Interpreter". You can use different interpreters for different files.**

<!-- Status badge from GitHub action checking validity of CITATION.cff -->
<!-- TODO: Amend the URL to your repository -->
[![Valid CITATION.cff](https://github.com/pythonhealthdatascience/stars_reproduction_template/actions/workflows/cff_validation.yaml/badge.svg)](https://github.com/pythonhealthdatascience/stars_reproduction_template/actions/workflows/cff_validation.yaml)

This repository forms part of work package 1 on the project STARS: Sharing Tools and Artefacts for Reproducible Simulations. It assesses the computational reproducibility of:

<!-- TODO: Amend to citation for the original study -->
> [Authors]. **[Title]**. *[Journal]* [Volume], [Edition] ([Year]). <[URL]>.

## Website

<!-- TODO: Amend the URL to your website -->
⭐ **[Click here to check out the website for this repository](https://pythonhealthdatascience.github.io/stars_reproduction_template/)** ⭐

This website is created using Quarto and hosted using GitHub Pages. It shares everything from this computational reproducibility assessment, displaying:
* The original study article and associated artefacts.
* Code and documentation from reproduction of the model.
* Evaluation of model reproduction success.
* Evaluation of the original study against guidelines for sharing research, criteria for journal reproducibility guidelines, and article reporting guidelines.
* Logbook with chronological entries detailing reproduction work.
* Final report describing the computational reproducibility assessment.

## Repository overview

<!-- TODO: Update this if you amend the structure or contents of the repository -->
```bash
├── .github
│   └──  workflows
│        └──  ...
├── evaluation
│   └──  ...
├── logbook
│   └──  ...
├── original_study
│   └──  ...
├── quarto_site
│   └──  ...
├── reproduction
│   └──  ...
├── .gitignore
├── CHANGELOG.md
├── CITATION.cff
├── CONTRIBUTING.md
├── LICENSE
├── README.md
├── _quarto.yml
├── citation_apalike.apa
├── citation_bibtex.bib
├── index.qmd
└── requirements.txt
```

**Key sections:** These folders have all the content related to the original study and reproduction...

* **`original_study/`** - Original study materials (i.e. journal article, supplementary material, code and any other research artefacts).
* **`reproduction/`** - Reproduction of the simulation model. Once complete, this functions as a research compendium for the model, containing all the code, parameters, outputs and documentation.
* **`evaluation/`** - Quarto documents from the evaluation of computational reproducibility. This includes the scope, assessment of reproduction success, and comparison of the original study materials against various guidelines, and summary report.
* **`logbook/`** - Daily record of work on this repository.

**Other sections:** The remaining files and folders support creation of the Quarto site to share the reproduction, or are other files important to the repository (e.g. `README`, `LICENSE`, `.gitignore`)...

* `.github/workflows/` - GitHub actions.
* `quarto_site/` - A Quarto website is used to share information from this repository (including the original study, reproduced model, and reproducibility evaluation). This folder contains any additional files required for creation of the site that do not otherwise belong in the other folders.
* `.gitignore` - Untracked files.
* `CHANGELOG.md` - Description of changes between GitHub releases and the associated versions on Zenodo.
* `CITATION.cff` - Instructions for citing this repository, created using [CFF INIT](https://citation-file-format.github.io/).
* `CONTRIBUTING.md` - Contribution instructions for repository.
* `LICENSE` - Details of the license for this work.
* `README.md` - Description for this repository. You'll find a seperate README for the model within the `reproduction/` folder, and potentially also the `original_study/` folder if a README was created by the original study authors.
* `_quarto.yml` - Set-up instructions for the Quarto website.
* `citation_apalike.bib` - APA citation generated from CITATION.cff.
* `citation_bibtex.bib` - Bibtex citation generated from CITATION.cff.
<!-- TODO: Remove this once it has been made into an action -->
* `docker_ghr.md` - Command for GitHub action to upload Docker image to GitHub container repository (converted into an action once a Dockerfile has been created)
* `index.qmd` - Home page for the Quarto website.
* `requirements.txt` - Environment for creation of Quarto site (used by `.github/workflows/quarto_publish.yaml`).

## Citation

If you wish to cite this repository, please refer to the citation file `CITATION.cff`, and the auto-generated alternatives `citation_apalike.apa` and `citation_bibtex.bib`.

## License

<!-- TODO: Add license name and link -->
This repository is licensed under the [license and link to file].

<!-- TODO: Add license name and link (e.g. "who also licensed their work under the [MIT License](link)") -->
This is aligned with the original study, who [license and link to file].

## Funding

This work is supported by the Medical Research Council [grant number MR/Z503915/1].