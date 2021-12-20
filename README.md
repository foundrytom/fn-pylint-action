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

## `pylint-ignore-paths`

The paths to pass to `pylint`s `--ignore-paths` command-line option.

## Example usage
```yaml
uses: TheFoundryVisionmongers/fn-pylint-action@v1
with:
  pylint-disable: "C,I,R"  # Only errors and warnings.
  pylint-rcfile: "./pyproject.toml"
  pylint-paths: "python tests"
```

## License

This project is licence under the [Apache 2.0 license](LICENSE), and
contains dependencies licence as per [dist/licenses.txt](dist/licenses.txt).
