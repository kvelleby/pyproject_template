# My project
  **<div style="text-align: right">A new project</div>**

## Installation

Requirements: ...

1. Install [mamba](https://github.com/conda-forge/miniforge#mambaforge).

2. Add [conda-lock](https://github.com/conda/conda-lock) to the base environment.

``` console
$ mamba install --channel=conda-forge --name=base conda-lock
```

3. Install [git](https://git-scm.com/downloads).

4. Download our package from github:

```console
$ git clone https://github.com/prio-data/<project_name>
$ cd <project_name>
```

1. Create the virtual environment based on lock-file created from environment.yml

``` console
$ conda-lock install -n my_project_env  --mamba
$ mamba activate my_project_env
```

6. Run poetry to add additional python package requirements.

```console
(my_project_env) $ poetry install
```

7. Add dependencies you cannot install with pip in "environment.yml" and everything else using poetry.

```console
(my_project_env) $ poetry add numpy
```

8. Write documentation using Markdown and Sphinx with the MyST parser.
