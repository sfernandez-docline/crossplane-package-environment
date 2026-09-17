## [0.6.2](https://github.com/sfernandez-docline/crossplane-package-environment/compare/v0.6.1...v0.6.2) (2026-09-17)

### Bug Fixes

* **folders-bootstrap:** activeDeadlineSeconds — el CronJob se atascaba para siempre ([#9](https://github.com/sfernandez-docline/crossplane-package-environment/issues/9)) ([6d14d91](https://github.com/sfernandez-docline/crossplane-package-environment/commit/6d14d916e96a4a9a405f5c40fc574e603013b33b))
* **netpol:** SMTP saliente a SES en non-live — el correo moría en timeout de conexión ([#8](https://github.com/sfernandez-docline/crossplane-package-environment/issues/8)) ([bb53e05](https://github.com/sfernandez-docline/crossplane-package-environment/commit/bb53e05024d20a11babdc62505b78eda3537ae57))

## [0.6.1](https://github.com/sfernandez-docline/crossplane-package-environment/compare/v0.6.0...v0.6.1) (2026-07-29)

### Bug Fixes

* **folders-bootstrap:** horario + imagen con curl/jq + tolerar desalojos ([b017b4e](https://github.com/sfernandez-docline/crossplane-package-environment/commit/b017b4ed6336414fc835998bfc898b62aaf84d72))
* **release:** tag de imagen v-prefijado (v${version}) al invocar build-xpkg ([#6](https://github.com/sfernandez-docline/crossplane-package-environment/issues/6)) ([b0f6c2c](https://github.com/sfernandez-docline/crossplane-package-environment/commit/b0f6c2c20915b0d729c645f9b8ab2b2bb974563e))

## [0.6.0](https://github.com/sfernandez-docline/crossplane-package-environment/compare/v0.5.4...v0.6.0) (2026-07-07)

### Features

* emit FinOps labels en el namespace infra-<env> ([1fc3f32](https://github.com/sfernandez-docline/crossplane-package-environment/commit/1fc3f324391e35510e62a6e147303d3a148ba6ab))
* **env:** core-egress-common egress completo en nonlive (MySQL/RMQ/valkey/HTTPS/same-ns) ([#5](https://github.com/sfernandez-docline/crossplane-package-environment/issues/5)) ([417b2ce](https://github.com/sfernandez-docline/crossplane-package-environment/commit/417b2cea68248f832bc8eeb8daa03255e5290762))
* **environment:** emitir NetworkPolicies de Atlas (operator ingress + db egress) ([7f2c264](https://github.com/sfernandez-docline/crossplane-package-environment/commit/7f2c264058b06db3aa61421e499b76b9034b24cc))

## [0.5.0](https://github.com/sfernandez-docline/crossplane-package-environment/compare/v0.4.6...v0.5.0) (2026-05-23)

### Features

* **pgbouncer:** emit Secret pg-env-roles-<env> directly to pgbouncer ns with labels ([d314176](https://github.com/sfernandez-docline/crossplane-package-environment/commit/d314176f74481efcf9e436799818eabf6352df49))

## [0.4.0](https://github.com/sfernandez-docline/crossplane-package-environment/compare/v0.3.0...v0.4.0) (2026-05-18)

### Features

* **pg-env-roles bridge:** annotate template para Reflector → pgbouncer ([70b87c9](https://github.com/sfernandez-docline/crossplane-package-environment/commit/70b87c920fcd22c79b6d48dce68d37150f67661d))
