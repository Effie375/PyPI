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

### Step 2: Download PIP get-pip.py

Before installing PIP, download the get-pip.py file: [get-pip.py](https://bootstrap.pypa.io/get-pip.py) on [pypa.io](https://bootstrap.pypa.io/get-pip.py).

Download the file to the desired folder in Windows. You can save the file to any location, but remember the path so you can use it later.

### Step 3: Launch Windows Command Line

PIP is a command-line program. When you install PIP, the PIP command is added to your system.

To launch the Command Prompt window:

- Press **Windows Key + X**.
- Click **Run**.
- Type in **cmd.exe** and hit enter.

Alternatively, type **cmd** in the Windows search bar and click the "Command Prompt" icon.

Both options open the Command Prompt window. However, note that you may need to run the Command Prompt "As Administrator." If you get an error at any point stating that you don’t have the necessary permissions to perform a task, you will need to open the app as admin.

To run the Command Prompt window "As Administrator", right-click "Command Prompt" and then select the "Run as…" option.

### Step 4: Installing PIP on Windows

Open the Command Prompt if it isn’t already open. Use the `cd` command followed by a folder name to navigate to the location of the get-pip.py file. This is the folder you previously used as the download location.

To install PIP type in the following:

```none
python get-pip.py
```

PIP installation should start. If the file isn’t found, double-check the path to the folder where you saved the file.

You can view the contents of your current directory using the following command:

```none
dir
```

The `dir` command returns a full listing of the contents of a directory.

### Step 5: How to Check PIP Version

To check the current version of PIP, type the following command:

```none
pip --version
```

This command returns the current version of the platform.

### Step 6: Verify Installation

Once you’ve installed PIP, you can test whether the installation has been successful by typing the following:

```none
pip help
```

If PIP has been installed, the program runs, and you should see:

```none
pip 18.0 from c:\users\administrator\appdata\local\programs\python\python37\lib\site-packages\pip (python 3.7)
```

If you receive an error, repeat the installation process.

### Step 6: Configuration

In Windows, the PIP configuration file is `%HOME%\pip\pip.ini`.

There is also a legacy per-user configuration file. The file is located at `%APPDATA%\pip\pip.ini`.

You can set a custom path location for this config file using the environment variable `PIP_CONFIG_FILE`.

#### Upgrading PIP for Python on Windows

New versions of PIP are released occasionally. These versions may improve the functionality or be obligatory for security purposes.

You can upgrade PIP on Windows using the Command Prompt window.

To upgrade PIP on Windows, enter the following in the command prompt:

```none
python -m pip install --upgrade pip
```

This command first uninstalls the old version of PIP and then installs the most current version of PIP.

#### Downgrade PIP Version

This may be necessary if a new version of PIP starts performing undesirably.

If you want to downgrade PIP to a prior version, you can do so by specifying the version.

To downgrade PIP, enter:

```none
python -m pip install pip==18.1
```

You should now see the version of PIP that you specified.

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

## Installing virtualenv on Windows

virtualenv is used to manage Python packages for different projects. Using virtualenv allows you to avoid installing Python packages globally which could break system tools or other projects. You can install virtualenv using pip.

```none
py -m pip install --user virtualenv
```

## Creating a virtual environment

To create a virtual environment, go to your project’s directory and run venv. If you are using Python 2, replace venv with virtualenv in the below commands.

```none
py -m venv env
```

The second argument is the location to create the virtual environment. Generally, you can just create this in your project and call it env.

venv will create a virtual Python installation in the env folder.

## Activating a virtual environment

Before you can start installing or using packages in your virtual environment you’ll need to activate it.

```none
.\env\Scripts\activate
```
