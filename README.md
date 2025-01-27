# Python-course

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/jboulanger/Python-course/HEAD)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jboulanger/Python-course)

This course introduces the essential steps of setting up an image analysis workflow for light microscopy data. It covers the topics of image loading, processing and quantification. It illustrates how to extract relevant information from an image using common Python packages.

To run the notebook on our local jupyter hub server copy and paste the following link into the browser: 

http://10.91.193.124/hub/user-redirect/git-pull?repo=https://github.com/jboulanger/Python-course&branch=main&app=lab

You can also use the badges at the top to open the repository on Google Colab and Binder.


## Installation

To run the notebook on your own computer, you need to install a few packages:

### Using miniconda
Install first [miniconda](https://docs.anaconda.com/free/miniconda/miniconda-install/).

On Windows with cuda support:
```bash
conda env create -f envs/environment-win.yml
conda activate imaging-python-course
```

On Linux with cuda support:
```bash
conda env create -f envs/environment-linux.yml
conda activate imaging-python-course
```

On MacOS:
```bash
conda env create -f envs/environment-macos.yml
conda activate imaging-python-course
```

### Using micromamba
In a terminal on Linux and MacOS or in a git bash terminal on MS Windows:

```bash
# install micromamba
"${SHELL}" <(curl -L micro.mamba.pm/install.sh)
# reload the shell
${SHELL}
# create an environment
micromamba -qy env create -f environment-linux.yml
# activate the environment 
micromamba activate imaging-python-course
# start the notebook
jupyter lab 
```

### Jupyterhub

Note that to have widgets working on jupyter lab, we need to install jupyterlab_widgets :

```bash
sudo -E -s
conda install -n base -c conda-forge jupyterlab_widgets
```

To install the environment:
```bash
sudo -E -s
conda env create -f envs/environment-linux.yml
```