# QuantUS-CEUS

[QuantUS](https://github.com/TUL-Dev/QuantUS) is an open-source quantitative analysis tool designed for ultrasonic tissue characterization (UTC) and contrast enhanced ultrasound (CEUS) imaging analysis. This repository contains all code behind the CEUS features of the software.

## Overview

In general, QuantUS provides an ultrasound system-independent platform for standardized, interactive, and scalable quantitative ultrasound research. The software is compatible on Mac OS X, Windows, and Linux.

This repository supports time intensity curve (TIC) analysis on 2D and 3D dynamic constrast enhanced ultrasound (DCE-US) cine loops. It uses lognormal curve fitting to compute the area under the curve (AUC), peak enhancement (PE), mean transit time (MTT), time to peak (TP), and normalization factor (TMPPV) parameters while also tracking the lesion area/volume. The software also includes functionality for 2D and 3D parametric map generation as well as motion compensation for 2D DCE-US analysis.

For more information, see our [documentation](https://tul-dev.github.io/PyQuantUS/).

![3D DCE-US Parametric Map Example](Images/3dDceusParamap.png)

## Requirements

* [Python](https://www.python.org/downloads/)

## Environment

First, download [Python3.11.8](https://www.python.org/downloads/release/python-3118/) (non-Conda version) from the Python website. Once installed, note its path. We will refer to this path as `$PYTHON` below.

Next, complete the following steps. Note lines commented with `# Unix` should only be run on MacOS or Linux while lines commented with `# Windows` should only be run on Windows.

```shell
git clone https://github.com/TUL-Dev/QuantUS.git
cd QuantUS
$PYTHON -m pip install virtualenv
$PYTHON -m virtualenv .venv
source .venv/bin/activate # Unix
.venv\Scripts\activate # Windows cmd
sudo apt-get update & sudo apt-get install python3-dev # Linux
pip install -r requirements.txt
```

Following this example, this environment can be accessed via the `source .venv/bin/activate`
command from the repository directory on Unix systems, and by `.venv\Scripts\activate` on Windows.

## Building

After configuring a Python virtual environment, finish preparing QuantUS to be run using the following commands:

```shell
# Using Python virtual env (Mac/Linux)
chmod +x saveQt.sh
./saveQt.sh

# Using Python virtual env (Windows)
ren saveQt.sh saveQt.bat
.\saveQt.bat
```

## Running

### Mac/Linux

```shell
source .venv/bin/activate
python main.py
```

### Windows

```shell
call .venv\scripts\activate.bat
python main.py
```

## Sample Data

[This folder](https://drive.google.com/drive/folders/1wZ1lAWxew0dqeIehVtiUIOOXQcaCT14p?usp=sharing)
contains minimal sample data required to get started with 2D and 3D CEUS analysis.
