# Contributing

This project operates a Pull Request model, using the [GitHub flow](https://guides.github.com/introduction/flow/index.html)
approach. The rough outline is as follows:

1. Chat with the Trusted Committers and community to define the scope of
   work
2. Fork the repo, and work in a branch
3. Create a Pull Request for Code Review
4. Address any comments
5. Work is merged

The main aim of the process is to keep people in the loop - avoiding any
surprises later on. This helps avoid churn/frustration for all involved.

More details on the development process will be provided soon. In the
meantime, please open an Issue or contact one of the Trusted Committers.

## Contribution sign off

`fn-pylint-action` is licensed under the [Apache 2.0 license](LICENSE). All
contributions to the project must abide by that license.

Contributions to the use of the [Developer’s Certificate of Origin 1.1 (DCO)](https://developercertificate.org).
All commits must be signed-off as follows, before merge, to indicate
that the submitter accepts the DCO:

```
Signed-off-by: Jóna Jónsdóttir <jona.jonsdottir@example.com>
```

This can be added automatically to a commit using `git commit -s`.

In addition, contributors are required to complete either the Individual
or Corporate Contribution License Agreement. Please contact one of the
trusted committers for more information.

## Releases

The action is released through CI, via the standard [GitHub Actions
release workflow](https://docs.github.com/en/actions/creating-actions/releasing-and-maintaining-actions#setting-up-github-actions-workflows).
This is taken care of by the workflow defined in
[release.yml](./.github/workflows/release.yml).  This will automatically
build and update the appropriate tags when a release is created in
GitHub.

The steps to follow are these:

1. Get a PR with the required changes reviewed and merged.
3. Update [CHANGES.md](CHANGES.md) accordingly with the new SemVer
   version.
4. Update [package.json](package.json) with the updated version.
5. Get a PR with these version changes reviewed and merged.
6. Create a release in the GitHub UI with the appropriate version,
   coping in the relevant changes from [CHANGES.md](CHANGES.md).

## Building manually

If you need to build the code locally for testing or a manual release,
the source + dependencies need to be bundled into the `dist` folder.
Assuming the current working directory contains `package.json` run:

```shell
npm install
npm run build
```

This will create a bundled build under `dist`, which is referenced by
the `action.yml`.


### IDE configuration

To aid in conforming to our coding style a [`.editorconfig`](https://editorconfig.org/)
file is included in the root of the repository, which has wide support
across various IDEs. For supported IDEs this config file can override
the default settings for inspections and formatting refactors.

In particular, more granular settings are included for IntelliJ-based
IDEs (for example, PyCharm) via the `ij_*` extensions.

## Trusted Committers

### Foundry
- @foundrytom [tom@foundry.com](mailto:tom@foundry.com)
- @feltech
