# flake8-bandit
[![Build Status](https://travis-ci.org/tylerwince/flake8-bandit.svg?branch=master)](https://travis-ci.org/tylerwince/flake8-bandit)

Automated security testing built right into your workflow!

You already use flake8 to lint all your code for errors, ensure docstrings are formatted correctly, sort your imports correctly, and much more... so why not ensure you are writing secure code while you're at it? If you already have flake8 installed all it takes is `pip install flake8-bandit`.

## Configuration

To include or exclude tests, use the standard `.bandit` configuration file. An example valid `.bandit` config file:

```text
[bandit]
exclude = /frontend,/scripts,/tests,/venv
tests: B101
```

In this case, we've specified to ignore a number of paths, and to only test for B101.

**Note:**  flake8-bugbear uses bandit default prefix 'B' so this plugin replaces the 'B' with an 'S' for Security. For more information, see https://github.com/PyCQA/flake8-bugbear/issues/37

## How's it work?

We use the [bandit](https://github.com/PyCQA/bandit) package from [PyCQA](http://meta.pycqa.org/en/latest/) for all the security testing.
