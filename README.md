# crossplane-package-environment

Crossplane Configuration package que define el XRD `Environment` parametrizado
por `spec.type` (`live` | `nonlive` | `ephemeral`).

## Por qué

Reemplaza los 3 paquetes históricos `crossplane-package-env-{live,nonlive,
ephemeral}` (90% código duplicado: Namespace + NetworkPolicy + opcional
bootstraps) por 1 unificado con branching por type. Una sola Composition KCL
aplica las políticas operacionales correspondientes:

| Type | Velero retention | deletionPolicy | autoPromote default |
|------|------------------|----------------|--------------------|
| live | 30d (720h) | Orphan | false |
| nonlive | 7d (168h) | Delete | true |
| ephemeral | disabled | Delete | true |

## Uso

```yaml
apiVersion: env.docline.io/v1alpha1
kind: Environment
metadata:
  name: int
spec:
  name: int
  type: nonlive
  stage: int
  zone: non-live
  parentEnvs: []
```

Aplica al cluster Hub (`control-ireland`). xflow Composition descubre los
Environments via `function-extra-resources` y genera Stages + Apps por
proyecto automáticamente.

## Instalación

```yaml
apiVersion: pkg.crossplane.io/v1
kind: Configuration
metadata:
  name: crossplane-package-environment
spec:
  package: ghcr.io/sfernandez-docline/crossplane-package-environment:<version>
```

## Recursos generados

Por cada `Environment` la Composition emite:

- `Namespace/<name>` con labels `env-type`, `stage`, `docline.io/environment`
- `NetworkPolicy/default-deny-all` (default deny ingress + egress)
- `Schedule/env-<name>-daily` Velero (si `type` permite backup)
- `XZonePostgreBoostrap/<name>` (si `spec.bootstrapPostgres=true`, default)
- `XZoneMysqlBoostrap/<name>` (si `spec.bootstrapMysql=true`, default)
- `XZoneRabbitmqBoostrap/<name>` (si `spec.bootstrapRabbitmq=true`, default)
