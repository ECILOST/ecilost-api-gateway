# ECILOST API Gateway

Punto de entrada transversal del sistema. Solo concentra políticas de borde: enrutamiento, CORS, correlación, límites de tasa, validación de JWT y observabilidad. Las reglas de subastas, catálogo, billetera y autenticación permanecen en sus respectivos servicios.

El esqueleto no declara rutas ni proxies: la documentación disponible no prueba todavía un contrato público consolidado. Las rutas se incorporarán desde configuración y contratos versionados, no mediante dependencias de bases de datos de los servicios.

```text
src/
  config/          Configuración transversal y destinos explícitos
  routing/         Adaptadores de enrutamiento, cuando haya contratos
  security/        JWT, CORS y rate limits
  observability/   Correlation ID, logs y métricas
```

El puerto local reservado es `8080`; Auth permanece en `3000`.
