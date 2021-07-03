# Python Package Index (PyPI)

## Introduction

**PIP** is a package management system used to install and manage software packages written in Python. It stands for "preferred installer program" or "Pip Installs Packages."

**PIP for Python** is a utility to manage PyPI package installations from the command line.

If you are using an older version of Python on Windows, you may need to install PIP. You can easily install PIP on Windows by downloading the installation package, opening the command line, and launching the installer.

This tutorial will show **how to install PIP on Windows**, check its version, upgrade, and configure.

**Note**: The latest versions of Python come with PIP pre-installed,  but older versions require manual installation. The following guide is for version 3.4 and above. If you are using an older version of Python, you can upgrade Python via the [Python website](https://www.python.org/downloads/).

## Installation

### Do I need to install pip?

**pip** is already installed if you are using Python 2 >=2.7.9 or Python 3 >=3.4 downloaded from [python.org](https://www.python.org/) or if you are working in a [Virtual Environment](https://packaging.python.org/tutorials/installing-packages/#creating-and-using-virtual-environments) created by [virtualenv](https://packaging.python.org/key_projects/#virtualenv) or [pyvenv](https://packaging.python.org/key_projects/#venv). Just make sure to [upgrade pip](https://pip.pypa.io/en/stable/installing/#upgrading-pip).

![Python Installation](images/python-installation.jpg)

## How To Install PIP To Manage Python Packages On Windows

### Prerequisites

- Computer running Windows or Windows server
- Access to the Command Prompt window

### Step 1: Check if PIP is Already Installed

Before you **install PIP on Windows**, check if PIP is already installed.

Type in the following command at the command prompt:

```none
pip help
```

If PIP responds, then PIP is installed. Otherwise, there will be an error saying the program could not be found.

### Installing with get-pip.py

To install pip, securely download [get-pip.py](https://bootstrap.pypa.io/get-pip.py) by following this link: get-pip.py. Alternatively, use `curl`:

```none
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
```

![Curl](images/curl.jpg)

Then run the following command in the folder where you have downloaded *get-pip.py*:

```none
python get-pip.py
```

![get-pip](images/get-pip.jpg)

### get-pip.py options

-	If set, do not attempt to install [setuptools](https://packaging.python.org/key_projects/#setuptools) (--no-setuptools)
-	If set, do not attempt to install [wheel](https://packaging.python.org/key_projects/#wheel) (--no-wheel)

![Get pip without wheel and setuptools](images/get-pip-without-wheel-setuptools.jpg)

## What is the easiest way to remove all packages installed by pip?

```none
pip freeze > requirements.txt
```

Now to remove one by one

```none
pip uninstall -r requirements.txt
```

If we want to remove all at once then

```none
pip uninstall -r requirements.txt -y
```

## The Python Package Installer

Install a package from PyPI:

```none
pip install SomePackage
```

Install a package from PyPI if the target machine doesn't have a network connection:

```none
pip install SomePackage-1.0-py2.py3-none-any.whl
```

Show what files were installed:

```none
pip show --files SomePackage
```

List what packages are outdated:

```none
pip list --outdated
```

Upgrade a package:

```none
pip install --upgrade SomePackage
```

Uninstall a package:

```none
pip uninstall SomePackage
```
