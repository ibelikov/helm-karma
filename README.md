# Karma

[Karma](https://github.com/prymitive/karma) is an Alert dashboard for [Prometheus Alertmanager](https://prometheus.io/docs/alerting/alertmanager/).

## Introduction

This chart bootstraps a [Karma](https://prometheus.io/) deployment on a [Kubernetes](http://kubernetes.io) cluster using the [Helm](https://helm.sh) package manager.

## Configuration

The following table lists the configurable parameters of the Karma chart and their default values.

Parameter | Description | Default
--------- | ----------- | -------
`image.repository` | karma container image repository | `lmierzwa/karma`
`image.tag` | karma container image tag | `v0.1.4`
`image.pullPolicy` | karma container image pull policy | `IfNotPresent`
`ingress.enabled` | If true, karma Ingress will be created | `false`
`ingress.annotations` | karma Ingress annotations | `{}`
`ingress.extraLabels` | karma Ingress additional labels | `{}`
`ingress.hosts` | karma Ingress hostnames | `[]`
`ingress.tls` | karma Ingress TLS configuration (YAML) | `[]`
`nodeSelector` | node labels for karma pod assignment | `{}`
`tolerations` | node taints to tolerate (requires Kubernetes >=1.6) | `[]`
`affinity` | pod affinity | `{}`
`replicaCount` | desired number of karma pods | `1`
`resources` | karma pod resource requests & limits | `{}`
`service.port` | karma service port | `8080`
`service.type` | type of karma service to create | `ClusterIP`
`config` | karma config file in yaml format. See [karma docs](https://github.com/prymitive/karma/blob/master/docs/CONFIGURATION.md) | `{}`
