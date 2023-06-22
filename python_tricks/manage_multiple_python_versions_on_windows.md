# How to manage multiple Python versions [Windows]?

# Install the needed Python versions

Before beginning to manage Python versions, you need to install them.

Select the desired versions having available binaries on the [official Python website](https://www.python.org/).

It is better to choose the python distribution corresponding to you system: x32 if it is a 32 bits system (uncommon nowadays) and x64 if 64 bits.

For instance, you can download the binaries for a recent python version [3.10.11](https://www.python.org/downloads/release/python-31011/) and those for a more recent one like [3.9.13](https://www.python.org/downloads/release/python-3913/).

Note that all the python release do not have pre-built binaries for windows.

Also be aware that you can not install two very close releases, such as python 3.9.13 and 3.9.16.
An error will be raised by the installer if you try it.
Hence, you have to limit yourself to major releases such as 3.8, 3.9, 3.10, 3.11, etc...

# Installing Python

Just as always, run the Python installer that you have downloaded.
Select the custom installation and check the "add to PATH" checkbox otherwise you will have to do it manually.

Adding a program (here Python) to PATH ensures that its executable is available directly without specifying its absolute path. It is very useful when programs have to be run through scripts and command lines.

Once done, there is only commands tricks...

# The special commands

## Checking installation

Now you know you have multiple Python versions installed.

You don't remember which one you chose.
Simply get to this folder by replacing \<Username> by your username:

```commandline
C:\Users\<Username>\AppData\Local\Programs\Python
```

You should see two folders now:

```commandline
C:\Users\<Username>\AppData\Local\Programs\Python\Python39
C:\Users\<Username>\AppData\Local\Programs\Python\Python310
```

Just check the respective versions with the following commands:

For Python 3.9

```commandline
py -3.9 --version
```

Same for Python 3.10:

```commandline
py -3.10 --version
```

You just confirmed both python versions are well installed.

# Run a Python script using a specific Python version

To run a Python file for instance called script.py using Python 3.9, just run:

```commandline
py -3.9 script.py
```

Same for Python 3.10:

```commandline
py -3.10 script.py
```

# Install packages for specific Python versions

Say you want to install packages using pip.

You have to choose the python version for which the package will be installed.

As an example, install the package matplotlib on Python 3.9 with:

```commandline
py -3.9 -m pip install matplotlib
```

Same for Python 3.10:

```commandline
py -3.10 -m pip install matplotlib
```

If you wish to specify the version of the package, choose the needed package version (here we choose version 1.0.1).
An operator should also be used to specify the tolerance for the installed version:
- ==  installs the specific version if compatible
- \>=  installs the specific version if compatible bu a more recent one can also be downloaded

For instance, you can install matplotlib (at least version 1.0.1) for Python 3.10 using this command:

```commandline
py -3.10 -m pip install matplotlib >= 1.0.1
```

# Using an IDE [Spyder, Pycharm, VSCode]

## Spyder


## PyCharm

In order to change or create a project with a specific python version in PyCharm, open the software. 
Here are some use cases:
- A environment folder is available at the root of the project. Either the

## VSCode

Simply open VSCode and then the Python file you wish to edit.
VSCode will auto-detect the python version.
Got to the bottom-right of the editor and click on the python version.
A menu will popup at the top, just select the right version.

Will be listed:
- Python base environments
- Python local virtual environments
- Conda environments...

Here, I've selected the anaconda environment for my project.

![[vs_code_choose_python_version.png]]