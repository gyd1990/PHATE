PHATE - Potential of Heat-diffusion for Affinity-based Transition Embedding
---------------------------------------------------------------------------

[![Latest PyPI version](https://img.shields.io/pypi/v/phate.svg)](https://pypi.org/project/phate/)
[![Latest CRAN version](https://img.shields.io/cran/v/phateR.svg)](https://cran.r-project.org/package=phateR)
[![Travis CI Build](https://api.travis-ci.com/KrishnaswamyLab/phate.svg?branch=master)](https://travis-ci.com/KrishnaswamyLab/PHATE)
[![Read the Docs](https://img.shields.io/readthedocs/phate.svg)](https://phate.readthedocs.io/)
[![bioRxiv Preprint](https://zenodo.org/badge/DOI/10.1101/120378.svg)](https://www.biorxiv.org/content/early/2017/12/01/120378)
[![Twitter](https://img.shields.io/twitter/follow/KrishnaswamyLab.svg?style=social&label=Follow)](https://twitter.com/KrishnaswamyLab)

PHATE is a tool for visualizing high dimensional single-cell data with natural progressions or trajectories. PHATE uses a novel conceptual framework for learning and visualizing the manifold inherent to biological systems in which smooth transitions mark the progressions of cells from one state to another. To see how PHATE can be applied to single-cell RNA-seq datasets from hematopoietic stem cells, human embryonic stem cells, and bone marrow samples, check out our preprint on BioRxiv.

[Kevin R. Moon, David van Dijk, Zheng Wang, et al. **PHATE: A Dimensionality Reduction Method for Visualizing Trajectory Structures in High-Dimensional Biological Data**. 2017. *BioRxiv*](http://biorxiv.org/content/early/2017/03/24/120378)


PHATE has been implemented in [Python](#python) (2.7 and >=3.5), [MATLAB](#matlab) and [R](#r).

### Table of Contents

* [Python](#python)
    * [Installation with pip](#installation-with-pip)
    * [Installation from source](#installation-from-source)
    * [Tutorial and Reference](#tutorial-and-reference)
* [MATLAB](#matlab)
    * [Installation](#installation)
    * [Tutorial and Reference](#tutorial-and-reference-1)
* [R](#r)
    * [Installation from CRAN and PyPi](#installation-from-cran-and-pypi)
    * [Installation with devtools and reticulate](#installation-with-devtools-and-reticulate)
    * [Installation from source](#installation-from-source-1)
    * [Tutorial and Reference](#tutorial-and-reference-2)
* [Help](#help)

### Python

#### Installation with `pip`

The Python version of PHATE can be installed by running the following from a terminal:

        pip install --user phate

#### Installation from source

The Python version of PHATE can be installed from GitHub by running the following from a terminal:

        git clone --recursive git://github.com/KrishnaswamyLab/PHATE.git
        cd PHATE/Python
        python setup.py install --user

#### Tutorial and Reference

For more information, read the [documentation on ReadTheDocs](http://phate.readthedocs.io/) or view our tutorials on GitHub: [single-cell RNA-seq](http://nbviewer.jupyter.org/github/KrishnaswamyLab/PHATE/blob/master/Python/tutorial/EmbryoidBody.ipynb), [artificial tree](http://nbviewer.jupyter.org/github/KrishnaswamyLab/PHATE/blob/master/Python/tutorial/PHATE_tree.ipynb).

### MATLAB

#### Installation

1. The MATLAB version of PHATE can be accessed by running the following from a terminal:

        git clone --recursive git://github.com/KrishnaswamyLab/PHATE.git
        cd PHATE/Matlab

2. Add the PHATE/Matlab directory to your MATLAB path.

#### Tutorial and Reference

Run any of our `run_*` scripts to get a feel for PHATE. Documentation is available in the MATLAB help viewer.

### R

In order to use PHATE in R, you must also install the Python package.

#### Installation from CRAN and PyPi

Install `phateR` from CRAN by running the following code in R:

    install.packages("phateR")

Install `phate` in Python by running the following code from a terminal:

    pip install --user phate

If `python` or `pip` are not installed, you will need to install them. We recommend [Miniconda3](https://conda.io/miniconda.html) to install Python and `pip` together, or otherwise you can install `pip` from https://pip.pypa.io/en/stable/installing/.

#### Installation with `devtools` and `reticulate`

The development version of PHATE can be installed directly from R with `devtools`:

    if (!suppressWarnings(require(devtools))) install.packages("devtools")
    devtools::install_github("KrishnaswamyLab/phateR")

If you have the development version of `reticulate`, you can also install `phate` in Python by running the following code in R:

    devtools::install_github("rstudio/reticulate")
    reticulate::py_install("phate", pip=TRUE)

#### Installation from source

The latest source version of PHATE can be accessed by running the following in a terminal:

    git clone --recursive git://github.com/SmitaKrishnaswamy/PHATE.git
    cd PHATE/phateR
    R CMD INSTALL
    cd ../Python
    python setup.py install --user

If the `phateR` folder is empty, you have may forgotten to use the `--recursive` option for `git clone`. You can rectify this by running the following in a terminal:

    cd PHATE
    git submodule init
    git submodule update
    cd phateR
    R CMD INSTALL
    cd ../Python
    python setup.py install --user


#### Tutorial and Reference

For more information and a tutorial, read the [phateR README](https://github.com/KrishnaswamyLab/phateR). Documentation is available in the R help viewer with `help(phateR::phate)`.

### Help

If you have any questions or require assistance using PHATE, please contact us at <https://krishnaswamylab.org/get-help>.
