# helm-compose

## TL;DR;

```console
helm repo add nousefreak https://nousefreak.github.io/helm-charts
helm install my-release nousefreak/helm-compose
```

## Introduction

- https://github.com/NoUseFreak/helm-compose
- https://github.com/NoUseFreak/helm-charts

## Prerequisites

- Kubernetes 1.19+

## Installing the Chart

To install the chart with the release name `my-release`:

```console
helm repo add nousefreak https://nousefreak.github.io/helm-charts
helm install my-release nousefreak/helm-compose
```

These commands deploy helm-compose on the Kubernetes cluster in the default configuration. The [Parameters](#parameters) section lists the parameters that can be configured during installation.

> **Tip**: List all releases using `helm list`

## Uninstalling the Chart

To uninstall/delete the `my-release` deployment:

```console
helm delete my-release
```

The command removes all the Kubernetes components associated with the chart and deletes the release.

## Configuration

The following tables list the configurable parameters of the helm-compose chart and their default values.

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| services.db.command | string | `"--default-authentication-plugin=mysql_native_password"` |  |
| services.db.environment[0] | string | `"MYSQL_ROOT_PASSWORD=somewordpress"` |  |
| services.db.environment[1] | string | `"MYSQL_DATABASE=wordpress"` |  |
| services.db.environment[2] | string | `"MYSQL_USER=wordpress"` |  |
| services.db.environment[3] | string | `"MYSQL_PASSWORD=wordpress"` |  |
| services.db.expose[0] | int | `3306` |  |
| services.db.expose[1] | int | `33060` |  |
| services.db.image | string | `"mariadb:10.6.4-focal"` |  |
| services.db.restart | string | `"always"` |  |
| services.db.volumes[0] | string | `"db_data:/var/lib/mysql"` |  |
| volumes.db_data | string | `nil` |  |

Specify each parameter using the `--set key=value[,key=value]` argument to `helm install`.

Alternatively, a YAML file that specifies the values for the parameters can be provided while installing the chart. For example,

```console
helm install my-release -f values.yaml nousefreak/helm-compose
```
