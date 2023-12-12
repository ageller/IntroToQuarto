# Intro To Quarto

Quarto enables users to combine libraries and code from multiple languages (e.g., Python and R) within the same workflow and to generate sharable reports.  For those familiar with R, Quarto is the "next generation of R Markdown".   In this workshop we will explore Quarto using both Python and R within the same workflow, and learn how to convert the output to HTML, PDF (and other formats) to share with others.  


The example here explores stock prices for Hershey's (chocolate).  I downloaded the [data](HSY.csv) from Yahoo finance. 

## Installation

1. Install Quarto:

    Documentation from Quarto can be found [here](https://docs.posit.co/resources/install-quarto/).  I used downloaded the latest version from their GitHub repo [here](https://github.com/quarto-dev/quarto-cli/releases/).  Then I added the executable from `<base_dir>/src/bin/` to my PATH variable.

2. Install Python and R and related libraries

    I recommend that you use conda and create an environment for this.  (You can either work with [full Anaconda](https://www.anaconda.com/download) or [miniconda](https://docs.conda.io/projects/miniconda/en/latest/).)  To create the environment:

```
conda create --name quarto-env
conda activate quarto-env
conda config --add channels conda-forge
conda config --set channel_priority strict
conda install python=3.10 r-base=4.1.3 pandas matplotlib numpy scipy r-rmarkdown r-reticulate
```

3. Before using Quarto, you will need to activate you env using `conda activate quarto-env`

## Rendering your Quarto doc to different formats

To convert `quarto_example.qmd` into a .html file using Quarto:

```
quarto render quarto_example.qmd --to html
```

(You can replace html with [many other formats](https://quarto.org/docs/output-formats/all-formats.html).)
