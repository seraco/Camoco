Camoco
======
[![Build Status](https://travis-ci.org/schae234/Camoco.svg?branch=master)](https://travis-ci.org/schae234/Camoco)
[![Coverage Status](https://coveralls.io/repos/schae234/Camoco/badge.svg?branch=master&service=github)](https://coveralls.io/github/schae234/Camoco?branch=master)


Co-Analysis of Molecular Components
-----------------------------------

Camoco is a python library for building and analyzing co-expression networks.
It creates co-expression networks from tablular formatted expression data and
common genome data files:

Required Files:
+ FPKM (or equivalent) CSV/TSV file
+ GFF File

Optional Files:
+ Gene Ontology (.obo and gene mapping)

Once co-expression networks are built, you can interact with the data using
the included command line:

```
source activate camoco
camoco --help
```
See more examples below in the CLI section.

or by using the package within a script
```
import camoco as co
```

Installation
------------
The best way to install Camoco is to use the included installation script.
This script creates an anaconda based virtual environment which takes care of
all required python packages as well as several of the external binaries and 
programs used by Camoco. Installation should be as easy as:

```
# Download and run install script
git clone https://github.com/schae234/Camoco.git
cd Camoco
# Follow instructions on screen
./install.sh
# Activate the virtual environment
source activate camoco
# Use CLI or run script
camoco --help
# deactivate virtual environment
source deactivate
```

You will need to add a few lines to your .bashrc in order for the conda environment
to be available from your shell.


e.g.:
```
# Assuming your installed camoco to ~/.camoco
export LD_LIBRARY_PATH=~/.camoco/lib/:$LD_LIBRARY_PATH
export PATH=$BASE/bin:~/.camoco/conda/bin/:$PATH
```

The installation script accepts simple arguments:
`-b (default: ~/.camoco)`: the base directory to install camoco including storage for databases

Tagged releases are available on PyPi: `pip install camoco`.

CLI
---
Once installed, the `camoco` command will be available through the terminal. See `camoco --help` for options!


Tests
-----
Unit tests within Camoco are implemented using the pytest framework. Unit tests
as well as Build tests can be found in the test directory.

Tests can be run by executing py.test in the tests dir:

```
source activate camoco
cd tests
py.test
```

Documentation
-------------
We acknowledge a lack of formal manual. We are writing this. However, the function definitions
themselves are well commented throughout the code base. Questions and concerns about usage issued
through github will be addressed! Contact us!

CacheMoneyCorn
--------------
