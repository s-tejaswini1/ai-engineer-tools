# UV commands

## Installation

- Run `sudo apt update` to update all the ubuntu dependencies

- Go to `https://docs.astral.sh/uv/getting-started/installation/` for refencence

- Run `curl -LsSf https://astral.sh/uv/install.sh | sh`

## Project setup with UV

- check working directory `pwd`
- view all the files and folders in the current folder `ls`
- if you want to create a new project run the below commands

```bash
mkdir projectname
cd projectname
uv init
```

alternatively

```bash
uv init projectname
cd projectname
```

check the files `la`, and you see the below output

```bash
.python-version  README.md  main.py  pyproject.toml
```

## Virtual environment

It's a individual workspace for indiviual project to avoid conflicts between projects

### create a virtual environment

```bash
uv venv
```

### Activate the virtual environment

```bash
source .venv/bin/activate
```

## Install dependencies

### As it's a new project, use `uv` for package management by default

```bash
uv add <package-name>
```

You can the package by doing

```bash
uv pip freeze | grep <package-name>
```


- You can also see that <package-name> in `dependencies@pyproject.toml`

- You want to install a package but you dont' want to add to `pyproject.toml`

```bash
uv pip install <package-name>
```


### If the project was created by someone else using pip

- Find the `requirements.txt`
- Run `uv pip install -r requirements.txt`

### Remove

```bash
uv remove <packagename>
```

## IPyhton

Quickly test the python packages before dive into the implementation

### Run simple python

```bash
uvx ipython
```

### Run with packages

```bash
uvx --with <packagename> ipython
```

### Run with multiple package names

```bash
uvx --with packagename1 --with packagename2 ipython
or
uvx --with packagename1,packagename2 ipython
```
