![AppVersion: 1.0.0](https://img.shields.io/badge/AppVersion-1.0.0-informational?style=flat-square)

# times-square-ui

The front-end for Times Square, a parameterized notebook web viewer for the Rubin Science Platform

## Source Code

* <https://github.com/lsst-sqre/times-square-ui>

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` | Affinity rules for the times-square-ui deployment pod |
| autoscaling.enabled | bool | `false` | Enable autoscaling of times-square-ui deployment |
| autoscaling.maxReplicas | int | `100` | Maximum number of times-square-ui deployment pods |
| autoscaling.minReplicas | int | `1` | Minimum number of times-square-ui deployment pods |
| autoscaling.targetCPUUtilizationPercentage | int | `80` | Target CPU utilization of times-square-ui deployment pods |
| config.semaphorePath | string | `nil` | Semaphore API URL path (default is no Semaphore integration) |
| config.siteDescription | string | `"Times Square hosts Jupyter Notebooks that are rendered on the fly on the Rubin Science Platform."` | Description, used in HTML metadata |
| config.siteName | string | `"Times Square"` | Name, used in the HTML header |
| config.timesSquareApiPath | string | `"/times-square/api"` | Times Square API URL path |
| fullnameOverride | string | `""` | Override the full name for resources (includes the release name) |
| image.pullPolicy | string | `"Always"` | Pull policy for the times-square-ui image |
| image.repository | string | `"ghcr.io/lsst-sqre/times-square-ui"` | Image to use in the times-square-ui deployment |
| image.tag | string | `""` | Overrides the image tag whose default is the chart appVersion. |
| imagePullSecrets | list | `[]` | Secret names to use for all Docker pulls |
| ingress.annotations | object | `{}` | Additional annotations for the ingress rule |
| ingress.enabled | bool | `true` | Create an ingress resource |
| ingress.gafaelfawrAuthQuery | string | `"scope=exec:notebook&auth_type=basic"` | Gafaelfawr auth query string |
| ingress.path | string | `"/times-square"` | URL path to dispatch to the times-square-ui deployment pod |
| ingress.pathType | string | `"ImplementationSpecific"` | Path type for the ingress rule |
| nameOverride | string | `""` | Override the base name for resources |
| nodeSelector | object | `{}` | Node selection rules for the times-square-ui deployment pod |
| podAnnotations | object | `{}` | Annotations for the times-square-ui deployment pod |
| replicaCount | int | `1` | Number of web deployment pods to start |
| resources | object | `{}` | Resource limits and requests for the times-square-ui deployment pod |
| service.port | int | `8080` | Port of the service to create and map to the ingress |
| service.type | string | `"ClusterIP"` | Type of service to create |
| tolerations | list | `[]` | Tolerations for the times-square-ui deployment pod |
