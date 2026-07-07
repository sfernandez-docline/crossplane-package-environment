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
