 ![SINDAN Project](https://raw.githubusercontent.com/SINDAN/sindan-docker/screenshot/logo.png)

# charts

[![BSD-3-Clause License](http://img.shields.io/github/license/SINDAN/charts)](LICENSE) [![Issues](https://img.shields.io/github/issues/SINDAN/charts)](https://github.com/SINDAN/charts/issues)
[![last commit](https://img.shields.io/github/last-commit/SINDAN/charts)](https://github.com/SINDAN/charts/commits) [![Releases](https://img.shields.io/github/release/SINDAN/charts)](https://github.com/SINDAN/charts/releases)  [![relase date](https://img.shields.io/github/release-date/SINDAN/charts)](https://github.com/SINDAN/charts/releases)

Official Chart repository for deploying [@SINDAN](https://github.com/SINDAN/) on kubernetes with Helm.

## Getting Started
Add this repository on your kubernetes environment.
```bash
$ helm repo add sindan-stable https://sindan.github.io/charts/stable
```
If the above installation was successful, you can search packages via `helm search` command.
```bash
$ helm repo list
$ helm search sindan
```

### List of Packages
| Name 	| Chart version 	| App version 	| Description 	|
|:----------------------------	|:--------------	|:------------	|:------------------------------------------------	|
| [sindan-stable/sindan-server](https://github.com/SINDAN/charts/tree/master/stable/sindan-server) 	| 0.9.0 	| 1.3.0 	| A Helm chart for server-side SINDAN suite (**TBD**) 	|

## Contributing
Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning
We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/SINDAN/charts/tags).

## Authors
- **Taichi MIYA** - *Initial work* - [@mi2428](https://github.com/mi2428)

See also the list of [contributors](https://github.com/SINDAN/charts/graphs/contributors) who participated in this project.

## License
This project is licensed under the BSD 3-Clause "New" or "Revised" License - see the [LICENSE](LICENSE) file for details.
