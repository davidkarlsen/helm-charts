# Adfinis Helm Charts

![Release Charts](https://github.com/adfinis-sygroup/helm-charts/workflows/Release%20Charts/badge.svg)

![Lunkwill wearing a Helm shirt](docs/images/lunkwill_helm_shirt.png)

This repository contains [Helm](https://helm.sh/) charts managed by [Adfinis](https://adfinis.com).

## Usage

### Install the Helm chart repository

```bash
helm repo add adfinis https://charts.adfinis.com
```

### Available Helm charts

| Chart | Description |
| ----- | ----------- |
| [argoconfig](charts/argoconfig) | Configure an Argo CD AppProject and Application |
| [barman](charts/barman) | Chart for Barman PostgreSQL Backup and Recovery Manager |
| [caasperli](charts/caasperli) | Deploy Caasperli to a Kubernetes Cluster |
| [kasperleyn](charts/kasperleyn) | A Helm 2 chart to deploy Caasperli |
| [timed](charts/timed) | Chart for Timed application |

## Development

### pre-commit hook

This project uses [pre-commit](https://pre-commit.com/) to automate some tasks like
generating README files.

#### pre-commit requirements

* [helm-docs](https://github.com/norwoodj/helm-docs)
* [gomplate](https://github.com/hairyhenderson/gomplate)

#### pre-commit configuration

After installing the pre-commit requirements you can initialize pre-commit.

```bash
pre-commit install
pre-commit install-hooks
```

## License

This Helm chart collection is free software: you can redistribute it and/or modify it under the terms
of the GNU Affero General Public License as published by the Free Software Foundation,
version 3 of the License.