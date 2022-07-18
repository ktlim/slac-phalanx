# cadc-tap-postgres

CADC TAP PostgresSQL service, used for ObsTAP

**Homepage:** <https://github.com/lsst-sqre/tap-postgres>

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` | Affinity rules for the cadc-tap-postgres pod |
| config.gcsBucket | string | None, must be set | Name of GCS bucket in which to store results |
| config.gcsBucketUrl | string | None, must be set | Base URL for results stored in GCS bucket |
| db.affinity | object | `{}` | Affinity rules for the database pod |
| db.image.pullPolicy | string | `"IfNotPresent"` | Pull policy for the database image |
| db.image.repository | string | `"lsstdax/tap-postgres-db"` | Database image to use |
| db.image.tag | string | The appVersion of the chart | Tag of database image to use |
| db.nodeSelector | object | `{}` | Node selection rules for the database pod |
| db.podAnnotations | object | `{}` | Annotations for the databse pod |
| db.resources | object | `{}` | Resource limits and requests for the database pod |
| db.tolerations | list | `[]` | Tolerations for the database pod |
| fullnameOverride | string | `"obstap"` | Override the full name for resources (includes the release name) |
| global.baseUrl | string | Set by Argo CD | Base URL for the environment |
| global.host | string | Set by Argo CD | Host name for ingress |
| global.vaultSecretsPath | string | Set by Argo CD | Base path for Vault secrets |
| image.pullPolicy | string | `"IfNotPresent"` | Pull policy for the tap image |
| image.repository | string | `"lsstdax/tap-postgres-server"` | tap-postgres image to use |
| image.tag | string | The appVersion of the chart | Tag of tap image to use |
| ingress.anonymousAnnotations | object | `{}` | Additional annotations to use for endpoints that allow anonymous access, such as `/capabilities` and `/availability` |
| ingress.authenticatedAnnotations | object | `{}` | Additional annotations to use for endpoints that are authenticated, such as `/sync`, `/async`, and `/tables` |
| ingress.gafaelfawrAuthQuery | string | `"scope=read:tap"` | Gafaelfawr auth query string |
| nameOverride | string | `""` | Override the base name for resources |
| nodeSelector | object | `{}` | Node selector rules for the cadc-tap-postgres pod |
| podAnnotations | object | `{}` | Annotations for the cadc-tap-postgres pod |
| replicaCount | int | `1` | Number of pods to start |
| resources | object | `{}` | Resource limits and requests for the cadc-tap-postgres pod |
| tolerations | list | `[]` | Tolerations for the cadc-tap-postgres pod |
| uws.affinity | object | `{}` | Affinity rules for the UWS database pod |
| uws.image.pullPolicy | string | `"IfNotPresent"` | Pull policy for the UWS database image |
| uws.image.repository | string | `"lsstdax/tap-postgres-uws"` | UWS database image to use |
| uws.image.tag | string | The appVersion of the chart | Tag of UWS database image to use |
| uws.nodeSelector | object | `{}` | Node selection rules for the UWS database pod |
| uws.podAnnotations | object | `{}` | Annotations for the UWS databse pod |
| uws.resources | object | `{}` | Resource limits and requests for the UWS database pod |
| uws.tolerations | list | `[]` | Tolerations for the UWS database pod |
