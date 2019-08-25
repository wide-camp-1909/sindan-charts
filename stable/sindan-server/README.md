# stable/sindan-server
This chart bootstraps a server-side [@SINDAN](https://github.com/SINDAN) environment on a Kubernetes cluster using the Helm package manager.  
**Current version is not suitable for production purpose. Please use with care.**

## Prerequisties
- Kubernetes 1.6 or later
- PV provisioner support in underlying infrastructure

## Install
To install the chart with release name `testing` in namespace `sindan-server`, please run the following.
```bash
$ helm install --name testing --namespace sindan-server stable/sindan-server
```
Check the release status with:
```bash
$ helm status testing
$ helm get testing
```

## Uninstall
To uninstall the release `testing`, please run the following.
```bash
$ helm delete testing
```
This command removes all components associated with the chart and delete the release.

## Configuration
The following table lists the configurable parameters and their default value.

| Parameter 	| Description 	| Default
|:---- 	|:---- 	|:----
| `ingress.enabled` | TBD | false
| `fluentd.image` | `fluentd` image repository | `sindan/fluentd`
| `fluentd.tag` | `fluentd` image tag | `1.3.0`
| `fluentd.pullPolicy` | `fluentd` image pull policy | `Always`
| `fluentd.servicePort` | `fluentd` listen port | 8080
| `mysql.image` | `mysql` image repository | `mysql`
| `mysql.tag` | `mysql` image tag | `5.7`
| `mysql.pullPolicy` | `mysql` image pull policy | `IfNotPresent`
| `mysql.db.name` | Database name | `sindan_production`
| `mysql.db.user` | Username granted to access the DB | `sindan`
| `mysql.db.password` | Password of the DB user | `cGFzc3dvcmQ=`
| `mysql.persistence.size` | Size of persistent volume claim | `2Gi`
| `mysql.persistence.storageClassName` | Type of persistent volume claim | `mysql`
| `mysqlbackup.cron.schedule` | Schedule of DB backup | `0 * * * *`
| `mysqlbackup.persistence.size` | Size of persistent volume claim | `2Gi`
| `mysqlbackup.persistence.storageClassName` | Type of persistent volume claim | `mysql-backup`
| `visualization.image` | `visualization` image repository | `sindan/visualization`
| `visualization.tag` | `visualization` image tag | `1.3.0`
| `visualization.pullPolicy` | `visualization` image pull policy | `Always`
| `visualization.rails.secretKeyBase` | Secret key base for decrypt configs | Default of `sindan/visualization`
| `visualization.webui.accounts` | Accounts of Web UI | User `sidnan` with password `changeme`
| `visualization.servicePort` | `visualization` listen port | 3000

## Persistence
This chart needs 2 PVs to persist `mysql` and `mysql-backup`.  
For example:
```bash
$ kubectl apply -f example/mysql-pv.yaml -f example/mysqlbackup-pv.yaml -n sindan-server
```
