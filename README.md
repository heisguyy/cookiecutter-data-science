# Cookiecutter Data Science

_A logical, reasonably standardized, but flexible project structure for doing and sharing data science work._


#### [Project homepage](http://drivendata.github.io/cookiecutter-data-science/)


### Requirements to use the cookiecutter template:
-----------
 - Python 2.7 or 3.5+
 - [Cookiecutter Python package](http://cookiecutter.readthedocs.org/en/latest/installation.html) >= 1.4.0: This can be installed with pip by or conda depending on how you manage your Python packages:

``` bash
$ pip install cookiecutter
```

or

``` bash
$ conda config --add channels conda-forge
$ conda install cookiecutter
```


### To start a new project, run:
------------

    cookiecutter https://github.com/heisguyy/cookiecutter-data-science


[![asciicast](https://asciinema.org/a/244658.svg)](https://asciinema.org/a/244658)

### New version of Cookiecutter Data Science
------------
Cookiecutter data science is moving to v2 soon, which will entail using
the command `ccds ...` rather than `cookiecutter ...`. The cookiecutter command
will continue to work, and this version of the template will still be available.
To use the legacy template, you will need to explicitly use `-c v1` to select it.
Please update any scripts/automation you have to append the `-c v1` option (as above),
which is available now.


### The resulting directory structure
------------

The directory structure of your new project looks like this: 
```

 ├── .github/workflows       <- CI/CD and automation files.
 │   ├── deploy.yml          <- Github action for continuous deployment (CD). 
 │   └── integration.yml     <- Github action for continuous integration tests (CI). 
 │── .vscode/settings.json   <- Visual studio code IDE config files.
 ├── artifacts               <- Trained and serialized models, vectorizers, encoders, tokenizers, etc.
 ├── data                    <- Data used for the project
 ├── experiments             <- Jupyter notebooks. Naming convention is a number (for ordering),
 │                              the creator's initials, and a short `-` delimited description, e.g.
 │                              `1.0-jqp-initial-data-exploration`.
 ├── infrastructure          <- IaC files.
 │   ├── modules/            <- Modules of various components of the deployment infrastructure.
 │   ├── vars/               <- Defined variables for stages of the development lifecycle.
 │   ├── main.tf             <- Terraform declaration of backend and infrastructure. 
 │   └── variables.tf        <- Terraform initialization of variables for the infrastructure.
 ├── src                     <- Source code for use in this project.
 │   ├── __init__.py         <- Makes src a Python module
 │   ├── main.py             <- Scripts for API.
 │   └── Dockerfile          <- Blueprint for building docker container.
 ├── tests                   <- Tests codes to ensure quality of codes. 
 │   ├── integration/        <- Codes to ensure changes haven't broken any essential feature.
 │   └── unit/               <- Codes to ensure that each function/unit is performing as expected.
 ├── .env                    <- Contains environmental variables like app secrets. This file should not
 │                              be committed or pushed.
 ├── .gitignore              <- List of files to avoid committing/pushing to the local and remote git repo.
 ├── .pre-commit-config.yaml <- Configurations of checks to run before a commit is accepted.
 ├── LICENSE                 <- Permissions for the public on the use/distribution of the repo/project.
 ├── Makefile                <- Makefile with commands like `make requirements`.
 ├── README.md               <- The top-level README for developers using this project.
 ├── pyproject.toml          <- Makefile with commands like `make data` or `make train`
 └── requirements.txt        <- List of libraries/packages and their versions required for the project.
```

## Contributing

We welcome contributions! [See the docs for guidelines](https://drivendata.github.io/cookiecutter-data-science/#contributing).

### Installing development requirements
------------

    pip install -r requirements.txt

### Running the tests
------------

    py.test tests
