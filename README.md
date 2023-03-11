# Python Template

Template repository for Python projects. Uses [pdm](https://github.com/pdm-project/pdm) as the package manager.

## Usage

1. Rename [project](./project) to the desired project name
2. Update the `$PROJECT` variable in [Makefile](./makefile) to match step 1
3. Run `pdm init` to configure [pyproject.toml](./pyproject.toml)
4. Add source code to the renamed `project` folder
5. Run `make init` to install the project to a `pdm` virtual environment
6. You can execute commands from the `pdm` environment with `pdm run`

## Optional steps
* Setup CI - a template CircleCI config is provided in `.circeci/config.yml`
* Create `Makefile.config` - secrets or per-user configuration can go here.
  Template `Makefile.config.example` is under version control, but `Makefile.config`
  is in `.gitignore`. Add `$(CONFIG_FILE)` as a make dependencies for recipes that
  need vars from `Makefile.config`

## Misc

* Run `make help` to get a partial list of available make recipes
* A pytest mark, `ci_skip`, is provided to mark tests that should be skipped 
  during CI pipelines
