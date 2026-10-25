# Install a Python virtual environment

A virtual environment is highly recommended when coding because you do not need to update system libraries and will be able to contain newly installed software.

There are several commonly used virtual environments but I'll cover three here:

1. Conda: open-source and maintained by NumFocus, a non-profit entity
2. Anaconda: Anaconda Distribution & Miniconda are maintained by Anaconda, Inc.  Free to use for educational purposes
3. Venv: built-in for Python and supported by Python Software Foundation (PSF) License, free to use for all

Anaconda has a GUI install and it's easiest for new comers using Python, however, Anaconda takes a lot of space. In this class, we will use miniconda but you can use venv if you like.

## Install miniconda

For MacOS, follow instructions on: https://www.anaconda.com/docs/getting-started/miniconda/install/mac-cli-install

For Windows, follow: https://www.anaconda.com/docs/getting-started/miniconda/install/windows-gui-install

Make sure you update your environment variables in your runtime SHELL for MacOS or Windows setup.  Run the following in terminal to review the information it returns.

```bash
> conda -h

> conda info --envs
```

### Create a virtual environment for this class

```bash
> conda create --name py315 python=3.15 numpy pandas

> conda activate py315
> which python
> /opt/miniconda3/envs/py315/bin/python

> python -V
> Python 3.15.1
```

Your results may differ from what is shown here.