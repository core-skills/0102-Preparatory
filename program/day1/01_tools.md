[Overview](./00_overview.md) |
[The Tools](./01_tools.md) |
[Reproducibility](./02_reproducibility.md) |
[Code Etiquette](./03_code_etiquette.md) |

# Overview of the Tools

## Background

At a high level, computers do four things:
* run programs
* store data
* communicate with each other, and
* interact with us

Your main challenge when using a computer is translating what you want to do and how you think about this in human language to something the computer can understand in machine language. For simple tasks the user interface is great as you simply point and click, however, this workflow is not easy to automate.

Programming languages help you instruct the computer on what to do, but many languages designed to work well with the computer are harder for us to learn. These are low-level<sup><a id="a1">[1](#f1)</a></sup> languages like C or FORTRAN. In contrast, high-level<sup><a id="a2">[2](#f2)</a></sup> languages, like Python or R, are designed to be easy to read and take away a lot of computational concerns like memory management.

<b id="f1">Low Level Language:</b> A [low-level language](https://www.computerhope.com/jargon/l/lowlangu.htm) is a programming language that provides little or no abstraction of programming concepts and is very close to writing actual machine instructions.  [↩](#a1)

<b id="f2">High Level Language:</b> In computer science, a [high-level programming language](https://en.wikipedia.org/wiki/High-level_programming_language) is a programming language with strong abstraction from the details of the computer.  [↩](#a2)

## Tools

All of the tools described below have been introduced during the pre-req and can be used in either the Windows, Mac or Linux operating systems.

### Anaconda

Anaconda is a distribution of Python and R bundled with commonly used packages for science and data science. It includes a package and environment management system, conda, and also offers integration with various programming user interfaces.

* Jupyter Notebook and JupyterLab

  Jupyter Notebook is a web-based, interactive computational environment which enables the user to develop code and write explanatory markdown to share their results and work. JupyterLab is based on the Jupyter Notebook, but offers a more extensive development environment in which one can launch notebooks, bash shells, or direct interfaces to a programming language.

* Python

  A high-level, interpreted programming language widely used for data science and machine learning. It is an open-source language and many of its packages are developed by community groups.

* Conda

  Conda enables the creation of dedicated programming environments for projects to separate potential issues of incompatible/different versions of packages between projects. It can also be used from the command line to
  download and update packages from a central repository.

### Git

Git is a version control system which keeps track of changes made to files within a repository, it also tracks useful metadata about these changes. Git is distributed, meaning it does not need to be hosted in a centralised server, but instead each contributor owns their own copy of the repository. Git is a program that can be called from the command line, but there are also various graphical user interfaces available.

**Github** is a hosting **service** where a Git repository can be stored and shared with other contributors or the community at large.

**GitKraken** is a **graphical user interface** (GUI) to git which can connect to your local and remote repositories, helping you keep track of your repositories.

### The Shell + Bash

The shell is a program which runs other programs instead of doing it’s own calculation. Bash is one of many Shell flavours. It is a simple language which works on the read-evaluate-print loop (REPL) paradigm. Bash is great for automating tasks using scripts<sup><a id="a3">[3](#f3)</a></sup>, which promotes reproducibility.

<b id="f3">Script:</b> In computer programming, a [script](https://whatis.techtarget.com/definition/script) is a sequence of instructions which are carried out by another program/ programming language rather than by the computer processor. [↩](#a3)

## Project Setup

Projects often come with different requirements, both on the data and computing front. Having a good project workflow and set up will help with managing these different requirements. Things to consider include:

1. Data Management

  * What type of data are you dealing with?
  * Where is the data stored?
  * How do you handle/process the data?

2. Folder Structure

  * Having a standard folder structure will make it easier to keep projects separated and find things.
  * Consider separating ongoing and completed work.
  * You should structure your folders hierarchically, starting with broader topics and creating more specific folders within these, e.g. `Projects > inProgress > ProjectName > docs, code, data, outputs`

3. Naming Conventions

  * Follow a naming convention within your folder structure, e.g. have the docs, code, data, and outputs folders in all of your projects.
  * Think about how you will work with your data, many programming languages do not like spaces in file names, you could use underscores instead

4. Documentation

  * Probably the simplest way to document your structure for your future reference - is to add a "README" file (a text file outlining the contents of the folder).
  * Also consider documenting your workflow.

## Programming Structure and Packages

When you run programming commands interactively, e.g. via a command line interpreter, definitions, like functions and variables, you have set up are lost once you quit the session. Thus, once you start writing longer programs you should save your analysis/commands in a text file which is known as a script. Scripts are organised into various modular subunits to simplify code maintenance and reuse. Functions are named sections of code which perform specific tasks.

Continuously adding to a script will create a file that becomes hard to maintain and it is best to split this into smaller files. Multiple related Python functions may be grouped together, with or without executable statements, in a `.py` file to create a module. A
module has a name and can be loaded into a python script or interactive session using an
`import` statement. To find out more on modules please have a look at the [Python documentation](https://docs.python.org/3/tutorial/modules.html).

Multiple modules can be grouped together into packages. The terms package and library are synonymous in Python, and packages are just a special kind of module. Package
structure is usually defined by directories and subdirectories containing `__init__.py` files. Subpackage names are separated from their parent package name by dots. Alternatively, subpackages can be imported directly with `from x import y` syntax. If you want to try your hand at creating a package you can follow the [Python packaging tutorial](https://packaging.python.org/tutorials/packaging-projects/).

You should utilise existing packages in your scripts wherever feasible to avoid reinventing the wheel. Popular, well established packages are usually more reliable and efficient than code you could write yourself. Package managers are used to simplify the distribution and installation of packages throughout the community.

## Package Management and Environments

Software and packages have different versions, this is only natural as they are continuously developed. However, different software and packages can have different conflicting dependencies on other software and packages.

Imagine you need package `X` for one of your projects. This package might depend on another package `Y` version 1. For another project you need package `Z`, however, this depends on version 2 of package `Y`. How do you manage the potential conflict?

Environment managers, such as `conda`, allow you to set up independent software environments for each of your projects. This way you can install package `X` with
dependency on version 1 of package `Y` in one environment and package `Z` with dependency on version 2 of package `Y` in another environment.

`conda` is also a package manager, which means you can use it to download and install the above mentioned packages. `pip` is the main Python package manager, but it doesn't manage environments, and it is a good idea to use it in conjunction with either `conda` or
another environment manager such as `venv`. To learn more you can check out the ["Understanding Conda and Pip" article on the Anaconda webpage](https://www.anaconda.com/understanding-conda-and-pip/).

[Overview](./00_overview.md) |
[The Tools](./01_tools.md) |
[Reproducibility](./02_reproducibility.md) |
[Code Etiquette](./03_code_etiquette.md)
