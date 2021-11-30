# fn-pylint-action

A GitHub Action to run `pylint`

This action executes [Pylint](https://pylint.pycqa.org/en/latest) on the
codebase and reports a summary in the action log and annotations on
source lines of a PR.

It is assumed that `pylint` is already installed in the environment.

## Inputs

## `pylint-paths`

**Required** The paths to instruct `pylint` to scan, space-separated.

## `pylint-rcfile`

Pylint configuration file location. Specifically, the value of
`pylint`'s `--rcfile=` command-line option.

## `pylint-disable`

Pylint checks to disable. Specifically, the value of `pylint`'s
`--disable=` command-line option.

## Example usage
```yaml
uses: TheFoundryVisionmongers/fn-pylint-action
with:
  pylint-disable: "C,I,R"  # Only errors and warnings.
  pylint-rcfile: "./pyproject.toml"
  pylint-paths: "python tests"
```

## Building

For more information on the GitHub Actions build and release workflow,
see the [official documentation](https://docs.github.com/en/actions/creating-actions/creating-a-javascript-action).

To bundle the source for use as a GitHub Action, assuming the current
working directory contains `package.json` run
```shell
npm install
npm run build
```
This will create a bundled build under `dist`, which is referenced by
the `action.yml`.

## License

This project is licenced under the [Apache 2.0 license](LICENSE), and
contains dependencis licenced as per [dist/licenses.txt](dist/licenses.txt).
