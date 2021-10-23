# clusterfan

## TL;DR;

```console
helm repo add nousefreak https://nousefreak.github.io/helm-charts
helm install my-release nousefreak/clusterfan
```

## Introduction

- https://github.com/NoUseFreak/clusterfan
- https://github.com/NoUseFreak/helm-charts

## Prerequisites

- Kubernetes 1.19+

## Installing the Chart

To install the chart with the release name `my-release`:

```console
helm repo add nousefreak https://nousefreak.github.io/helm-charts
helm install my-release nousefreak/clusterfan
```

These commands deploy clusterfan on the Kubernetes cluster in the default configuration. The [Parameters](#parameters) section lists the parameters that can be configured during installation.

> **Tip**: List all releases using `helm list`

## Uninstalling the Chart

To uninstall/delete the `my-release` deployment:

```console
helm delete my-release
```

The command removes all the Kubernetes components associated with the chart and deletes the release.

## Configuration

The following tables list the configurable parameters of the clusterfan chart and their default values.

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| image.repository | string | `"nousefreak/clusterfan"` |  |
| image.tag | string | `"v0.0.15"` |  |
| pwm.hostname | string | `"kmaster"` |  |

Specify each parameter using the `--set key=value[,key=value]` argument to `helm install`.

Alternatively, a YAML file that specifies the values for the parameters can be provided while installing the chart. For example,

```console
helm install my-release -f values.yaml nousefreak/clusterfan
```
