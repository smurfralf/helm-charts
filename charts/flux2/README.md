# flux2

![Version: 0.8.4](https://img.shields.io/badge/Version-0.8.4-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.24.1](https://img.shields.io/badge/AppVersion-0.24.1-informational?style=flat-square)

A Helm chart for flux2

This helm chart is maintain and released by the fluxcd-community on a best effort basis.

## Source Code

* <https://github.com/fluxcd-community/helm-charts>

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| cli.affinity | object | `{}` |  |
| cli.image | string | `"ghcr.io/fluxcd/flux-cli"` |  |
| cli.nodeSelector | object | `{}` |  |
| cli.tag | string | `"v0.24.1"` |  |
| cli.tolerations | list | `[]` |  |
| eventsaddr | string | `"http://notification-controller/"` | Maybe you need to use full domain name here, if you deploy flux in environments that use http proxy. In such environments they normally add `.cluster.local` and `.local` suffixes to `no_proxy` variable in order to prevent cluster-local traffic from going through http proxy. Without fully specified domain they need to mention `notifications-controller` explicitly in `no_proxy` variable after debugging http proxy logs eg: http://notification-controller.[NAMESPACE].svc.[CLUSTERDOMAIN] |
| helmcontroller.affinity | object | `{}` |  |
| helmcontroller.annotations."prometheus.io/port" | string | `"8080"` |  |
| helmcontroller.annotations."prometheus.io/scrape" | string | `"true"` |  |
| helmcontroller.create | bool | `true` |  |
| helmcontroller.image | string | `"ghcr.io/fluxcd/helm-controller"` |  |
| helmcontroller.labels | object | `{}` |  |
| helmcontroller.nodeSelector | object | `{}` |  |
| helmcontroller.resources.limits.cpu | string | `"1000m"` |  |
| helmcontroller.resources.limits.memory | string | `"1Gi"` |  |
| helmcontroller.resources.requests.cpu | string | `"100m"` |  |
| helmcontroller.resources.requests.memory | string | `"64Mi"` |  |
| helmcontroller.serviceaccount.annotations | object | `{}` |  |
| helmcontroller.serviceaccount.create | bool | `true` |  |
| helmcontroller.tag | string | `"v0.14.1"` |  |
| helmcontroller.tolerations | list | `[]` |  |
| imagePullSecrets | list | `[]` | contents of pod imagePullSecret in form 'name=[secretName]'; applied to all controllers |
| imageautomationcontroller.affinity | object | `{}` |  |
| imageautomationcontroller.annotations."prometheus.io/port" | string | `"8080"` |  |
| imageautomationcontroller.annotations."prometheus.io/scrape" | string | `"true"` |  |
| imageautomationcontroller.create | bool | `true` |  |
| imageautomationcontroller.image | string | `"ghcr.io/fluxcd/image-automation-controller"` |  |
| imageautomationcontroller.labels | object | `{}` |  |
| imageautomationcontroller.nodeSelector | object | `{}` |  |
| imageautomationcontroller.resources.limits.cpu | string | `"1000m"` |  |
| imageautomationcontroller.resources.limits.memory | string | `"1Gi"` |  |
| imageautomationcontroller.resources.requests.cpu | string | `"100m"` |  |
| imageautomationcontroller.resources.requests.memory | string | `"64Mi"` |  |
| imageautomationcontroller.serviceaccount.annotations | object | `{}` |  |
| imageautomationcontroller.serviceaccount.create | bool | `true` |  |
| imageautomationcontroller.tag | string | `"v0.18.0"` |  |
| imageautomationcontroller.tolerations | list | `[]` |  |
| imagereflectorcontroller.affinity | object | `{}` |  |
| imagereflectorcontroller.annotations."prometheus.io/port" | string | `"8080"` |  |
| imagereflectorcontroller.annotations."prometheus.io/scrape" | string | `"true"` |  |
| imagereflectorcontroller.create | bool | `true` |  |
| imagereflectorcontroller.image | string | `"ghcr.io/fluxcd/image-reflector-controller"` |  |
| imagereflectorcontroller.labels | object | `{}` |  |
| imagereflectorcontroller.nodeSelector | object | `{}` |  |
| imagereflectorcontroller.resources.limits.cpu | string | `"1000m"` |  |
| imagereflectorcontroller.resources.limits.memory | string | `"1Gi"` |  |
| imagereflectorcontroller.resources.requests.cpu | string | `"100m"` |  |
| imagereflectorcontroller.resources.requests.memory | string | `"64Mi"` |  |
| imagereflectorcontroller.serviceaccount.annotations | object | `{}` |  |
| imagereflectorcontroller.serviceaccount.create | bool | `true` |  |
| imagereflectorcontroller.tag | string | `"v0.14.0"` |  |
| imagereflectorcontroller.tolerations | list | `[]` |  |
| installCRDs | bool | `true` |  |
| kustomizecontroller.affinity | object | `{}` |  |
| kustomizecontroller.annotations."prometheus.io/port" | string | `"8080"` |  |
| kustomizecontroller.annotations."prometheus.io/scrape" | string | `"true"` |  |
| kustomizecontroller.create | bool | `true` |  |
| kustomizecontroller.envFrom | object | `{"map":{"name":""},"secret":{"name":""}}` | Defines envFrom using a configmap and/or secret. |
| kustomizecontroller.extraSecretMounts | list | `[]` | Defines additional mounts with secrets. Secrets must be manually created in the namespace or with kustomizecontroller.secret |
| kustomizecontroller.image | string | `"ghcr.io/fluxcd/kustomize-controller"` |  |
| kustomizecontroller.labels | object | `{}` |  |
| kustomizecontroller.nodeSelector | object | `{}` |  |
| kustomizecontroller.resources.limits.cpu | string | `"1000m"` |  |
| kustomizecontroller.resources.limits.memory | string | `"1Gi"` |  |
| kustomizecontroller.resources.requests.cpu | string | `"100m"` |  |
| kustomizecontroller.resources.requests.memory | string | `"64Mi"` |  |
| kustomizecontroller.secret.create | bool | `false` | Create a secret to use it with extraSecretMounts. Defaults to false. |
| kustomizecontroller.secret.data | object | `{}` |  |
| kustomizecontroller.secret.name | string | `""` |  |
| kustomizecontroller.serviceaccount.annotations | object | `{}` |  |
| kustomizecontroller.serviceaccount.create | bool | `true` |  |
| kustomizecontroller.tag | string | `"v0.18.2"` |  |
| kustomizecontroller.tolerations | list | `[]` |  |
| notificationcontroller.affinity | object | `{}` |  |
| notificationcontroller.annotations."prometheus.io/port" | string | `"8080"` |  |
| notificationcontroller.annotations."prometheus.io/scrape" | string | `"true"` |  |
| notificationcontroller.create | bool | `true` |  |
| notificationcontroller.image | string | `"ghcr.io/fluxcd/notification-controller"` |  |
| notificationcontroller.labels | object | `{}` |  |
| notificationcontroller.nodeSelector | object | `{}` |  |
| notificationcontroller.resources.limits.cpu | string | `"1000m"` |  |
| notificationcontroller.resources.limits.memory | string | `"1Gi"` |  |
| notificationcontroller.resources.requests.cpu | string | `"100m"` |  |
| notificationcontroller.resources.requests.memory | string | `"64Mi"` |  |
| notificationcontroller.service.labels | object | `{}` |  |
| notificationcontroller.serviceaccount.annotations | object | `{}` |  |
| notificationcontroller.serviceaccount.create | bool | `true` |  |
| notificationcontroller.tag | string | `"v0.19.0"` |  |
| notificationcontroller.tolerations | list | `[]` |  |
| policies.create | bool | `true` |  |
| rbac.create | bool | `true` |  |
| sourcecontroller.affinity | object | `{}` |  |
| sourcecontroller.annotations."prometheus.io/port" | string | `"8080"` |  |
| sourcecontroller.annotations."prometheus.io/scrape" | string | `"true"` |  |
| sourcecontroller.create | bool | `true` |  |
| sourcecontroller.image | string | `"ghcr.io/fluxcd/source-controller"` |  |
| sourcecontroller.labels | object | `{}` |  |
| sourcecontroller.nodeSelector | object | `{}` |  |
| sourcecontroller.resources.limits.cpu | string | `"1000m"` |  |
| sourcecontroller.resources.limits.memory | string | `"1Gi"` |  |
| sourcecontroller.resources.requests.cpu | string | `"100m"` |  |
| sourcecontroller.resources.requests.memory | string | `"64Mi"` |  |
| sourcecontroller.service.labels | object | `{}` |  |
| sourcecontroller.serviceaccount.annotations | object | `{}` |  |
| sourcecontroller.serviceaccount.create | bool | `true` |  |
| sourcecontroller.tag | string | `"v0.19.2"` |  |
| sourcecontroller.tolerations | list | `[]` |  |
| watchallnamespaces | bool | `true` |  |
