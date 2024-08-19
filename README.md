ensure-chocolatey
==============

[GitHub Action](https://github.com/features/actions) to install the [Chocolatey
package manager](https://docs.chocolatey.org/en-us/) on Windows if it is not
already installed.

Since the [GitHub Windows runner images](https://github.com/actions/runner-images/blob/main/images/windows/Windows2022-Readme.md)
already have Chocolatey installed, this action is only useful when running
custom Windows runners that are not configured the same as the GitHub Windows
runners.

Inputs
------

- 'install-script': URL for the Chocolatey PowerShell installer script (default `https://community.chocolatey.org/install.ps1`).

License
-------

MIT License. See [LICENSE](LICENSE) for details.


Usage Example
-------------

```yaml
jobs:
  build:
    - uses: andrurogerz/ensure-chocolatey@main
    - run: choco install pester -version 2.0.2
```
