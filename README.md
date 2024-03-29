# Genomics data index examples
[![Binder](https://mybinder.org/badge_logo.svg)][tutorial1-binder]

This repository contains examples for the [genomics-data-index][] project, which is a system which can index large amounts of genomics data and enable rapid querying of this data.

**Indexing** breaks genomes up into individual features (*nucleotide mutations*, *kmers*, or *genes/MLST*)
and stores the index in a directory which can easily be shared with other people. Indexes can be generated 
direct from sequence data or loaded from existing intermediate files (e.g., VCF files).

```bash
# Index features in VCF files listed in vcf-files.txt
gdi load vcf vcf-files.txt
```

**Querying** provides both a *Python API* and *Command-line interface* to select sets of samples using this index
or attached external data (e.g., phylogenetic trees or DataFrames of metadata).

```python
# Select samples with a 26568 C > A mutation
r = s.hasa('MN996528.1:26568:C:A')
```

# Tutorial

Tutorials and a demonstration of the [genomics-data-index][] software are available below. You can select the **[launch | binder]** badge to launch each of these tutorials in an interactive [Jupyter][] environment within the cloud environment using [Binder][].

1. [Tutorial 1: Querying (Salmonella)][tutorial1] - [![Binder](https://mybinder.org/badge_logo.svg)][tutorial1-binder] 
    * _In case GitHub link is not rendering try [here][tutorial1-nbviewer]_
2. [Tutorial 2: Indexing assemblies (SARS-CoV-2)][tutorial2] - [![Binder](https://mybinder.org/badge_logo.svg)][tutorial2-binder]
    * _In case GitHub link is not rendering try [here][tutorial2-nbviewer]_
3. [Tutorial 3: Querying overview][tutorial3] - [![Binder](https://mybinder.org/badge_logo.svg)][tutorial3-binder]
    * _In case GitHub link is not rendering try [here][tutorial3-nbviewer]_

Alternatively, you can run these tutorials on your local machine. In order to run these tutorials you will first have to install the `genomics-data-index` software (see the [Installation][installation] section for details). In addition, you will have to install [Jupyter Lab][]. If you have already installed the `genomics-data-index` software with conda you can install Jupyter Lab as follows:

```bash
conda activate gdi
conda install jupyterlab
```

To run Jupyter you can run the following:

```bash
jupyter lab
```

Please see the instructions for [Jupyter Lab][jupyter-docs] for details on using Jupyter.


[genomics-data-index]: https://github.com/apetkau/genomics-data-index
[tutorial1]: examples/tutorial-1-salmonella.ipynb
[tutorial2]: examples/tutorial-2-sars-cov-2.ipynb
[tutorial3]: examples/tutorial-3-querying-overview.ipynb
[conda]: https://docs.conda.io/en/latest/
[bioconda]: https://bioconda.github.io/
[Jupyter Lab]: https://jupyter.org/
[Jupyter]: https://jupyter.org/
[jupyter-docs]: https://jupyterlab.readthedocs.io/en/latest/
[Binder]: https://mybinder.org/
[installation]: https://github.com/apetkau/genomics-data-index#3-installation
[tutorial1-nbviewer]: https://nbviewer.jupyter.org/github/apetkau/genomics-data-index-examples/blob/main/examples/tutorial-1-salmonella.ipynb
[tutorial2-nbviewer]: https://nbviewer.jupyter.org/github/apetkau/genomics-data-index-examples/blob/main/examples/tutorial-2-sars-cov-2.ipynb
[tutorial3-nbviewer]: https://nbviewer.jupyter.org/github/apetkau/genomics-data-index-examples/blob/main/examples/tutorial-3-querying-overview.ipynb
[tutorial1-binder]: https://mybinder.org/v2/gh/apetkau/genomics-data-index-examples/main?urlpath=lab%2Ftree%2Fexamples%2Ftutorial-1-salmonella.ipynb
[tutorial2-binder]: https://mybinder.org/v2/gh/apetkau/genomics-data-index-examples/main?urlpath=lab%2Ftree%2Fexamples%2Ftutorial-2-sars-cov-2.ipynb
[tutorial3-binder]: https://mybinder.org/v2/gh/apetkau/genomics-data-index-examples/main?urlpath=lab%2Ftree%2Fexamples%2Ftutorial-3-querying-overview.ipynb

