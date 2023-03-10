# Python Template

Template repository for Python projects.

## Usage

1. Rename `project` to the desired project name
2. Update the `$PROJECT` variable in `Makefile` to match step 1
3. Update `install_requires` in `setup.cfg` with project dependencies
4. Add source code to the renamed `project` folder
5. Run `make init` to install the project to a `pipenv` virtual environment
6. You can execute commands from the `pipenv` environment with `pipenv run`

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
