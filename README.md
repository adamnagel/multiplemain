📦 multiplemain
=======================

This repo is a fork of the well-known canonical 
[setup.py](https://github.com/navdeep-G/setup.py) example.

The purpose of this repo is to show how a `pip install`-able
Python module can expose multiple main functions. This would be
useful if you plan to expose multiple related capabilities in a
command-line-driven environment, as opposed to importing your
Python modules into other code.

The benefit is that you can have a single package to `pip install`,
while exposing multiple command-line functions, each with its own
option parsing, help text, and so on.

Installation
-----

```bash
cd <root directory of this repository>
pip install -e .
```

Demonstration
-----

```bash
% python -m multiplemain
This is multiplemain/__main__.py

% python -m multiplemain.alice
This is multiplemain/alice/__main__.py

% python -m multiplemain.bob
This is multiplemain/bob/__main__.py
```