<p align="center">
A <a href="https://github.com/audreyr/cookiecutter">cookiecutter</a> template for <a href="https://github.com/xonsh/xonsh">xonsh</a> contributions called <a href="https://xon.sh/xontribs.html">xontribs</a>.
</p>

<p align="center">
If you like the template click ⭐ on the repo.
</p>

## Why use this template?

This template includes good pack of prebuilt files:

* xontrib promotion instructions in the README
* `pyproject.toml` file to make and install PyPi package easily using [poetry](https://github.com/python-poetry/poetry/)
* `.gitattributes` file to enable Github syntax highlighting for `*.xsh` files
* `.gitignore` file with standard list of directories to ignore

## Create new xontrib

To create a `xontrib` from this template just run:

``` bash
pip install cookiecutter
cookiecutter gh:jnoortheen/xontrib-cookiecutter-poetry
```

## Example

``` bash
$ cookiecutter gh:jnoortheen/xontrib-cookiecutter-poetry
full_name [Your name]: Snail
email [Your address email]: snail@snail.snail
github_username [Your github username]: snail
project_name [Name of the project (for humans, without xontrib- prefix)]: my-super-xontrib
project_slug [my-super-xontrib]:
project_short_description [A short description of the project]: It's my super xontrib!
version [0.1.0]:

# optionally use github-cli to create repo
$ gh repo create

$ tree
.
`-- xontrib-my-super-xontrib
    |-- LICENSE
    |-- README.md
    |-- pyproject.toml
    `-- xontrib
        `-- my-super-xontrib.xsh

$ git push

$ poetry publish

# in your xonsh environment
$ pip install -U xontrib-my-super-xontrib/
Successfully installed xontrib-my-super-xontrib-0.1.0

$ xontrib load my-super-xontrib
This is my-super-xontrib!
```
