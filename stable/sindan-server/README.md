# stable/sindan-server
This chart bootstraps a server-side [@SINDAN](https://github.com/SINDAN) environment on a Kubernetes cluster using the Helm package manager.  
**Current version is not suitable for production purpose. Please use with care.**

## Prerequisties
TBD

## Installing the Chart
To install the chart with release name `testing` in namespace `sindan-server`, please run the following.
```bash
$ helm install --name testing --namespace sindan-server stable/sindan-server
```
Check the release status with:
```bash
$ helm status testing
$ helm get testing
```

## Uninstalling the Chart
To uninstall the release `testing`, please run the following.
```bash
$ helm delete testing
```
This command removes all components associated with the chart and delete the release.

## Configuration
TBD

## Persistence
TBD
