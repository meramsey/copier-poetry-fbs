# Copier Poetry

Copier template for Poetry FBS based projects.

This copier template is mainly for my own usage,
but feel free to try it out, or fork it!

## Features

- [Poetry](https://github.com/sdispater/poetry) setup, with pre-defined `pyproject.toml`
- [FBS](https://github.com/mherrmann/fbs) setup, with pre-defined `base.json` and other needed boilerplate and setup with .ui mainwindow and about dialog with Qsettings.
- Documentation built with [MkDocs](https://github.com/mkdocs/mkdocs)
  ([Material theme](https://github.com/squidfunk/mkdocs-material)
  and "autodoc" [mkdocstrings plugin](https://github.com/pawamoy/mkdocstrings))
- Pre-configured tools for code formatting, quality analysis and testing:
    - [black](https://github.com/psf/black),
    - [flakehell](https://github.com/life4/flakehell)
      ([flake8](https://gitlab.com/pycqa/flake8) wrapper) and plugins,
    - [isort](https://github.com/timothycrosley/isort),
    - [mypy](https://github.com/python/mypy),
    - [safety](https://github.com/pyupio/safety)
- Tests run with [pytest](https://github.com/pytest-dev/pytest) and plugins, with [coverage](https://github.com/nedbat/coveragepy) support
- Cross-platform tasks with [duty](https://github.com/pawamoy/duty)
- Support for GitHub workflow and Gitlab CI
- Python 3.6 or above
- Auto-generated `CHANGELOG.md` from git commits (using Angular message style)
- Auto-generated `CREDITS.md` from Python dependencies
- All licenses from [choosealicense.com](https://choosealicense.com/appendix/)
- Makefile for convenience

## Quick setup and usage

Make sure all the
[requirements](https://pawamoy.github.io/copier-poetry/requirements)
are met, then:

```bash
copier "https://gitlab.com/mikeramsey/copier-poetry-fbs.git" /path/to/your/new/project
```

Or even shorter:

```bash
copier "gl:mikeramsey/copier-poetry-fbs.git" /path/to/your/new/project
```

See the [documentation](https://pawamoy.github.io/copier-poetry)
for more details.

## Modifying the template skeleton usage
Once poetry venv is installed you can run the below to see the skeleton mainwindow.
```bash
fbs run
```

You can then add all your custom widgets and signals and slots easily to the `src/main/python/{{your_app}}/main.py` file.

To edit the GUI just open `src/main/python/{{your_app}}/ui/mainwindow.ui` file in Qt Designer and save and then rerun fbs run to see changes instantly.

## Helpful Resources
[fbs-documentation](https://build-system.fman.io/): FBS documentation for the fbs specific details.

[LearnPyQt](https://www.learnpyqt.com/): Has some of the best video tutorials and up to date resources for PyQT/Pyside.
