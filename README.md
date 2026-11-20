# ECILOST API Gateway

Proyecto base de NestJS para un futuro punto de entrada HTTP. El código actual arranca el proceso y carga configuración. El enrutamiento, la autenticación de borde y la observabilidad distribuida están pendientes de implementación.

## Inicio local

```bash
cp .env.example .env
npm install
npm run start:dev
```

El proceso escucha en `PORT`, con valor local por defecto `8080`. Aún no registra rutas HTTP ni publica Swagger. En desarrollo, el frontend usa su proxy de Vite para llamar directamente a Auth, Catalog, Wallet, Auction y Engagement.

## Estructura y comprobación

- [Enrutamiento](src/routing/README.md)
- [Políticas de seguridad previstas](src/security/README.md)
- [Observabilidad prevista](src/observability/README.md)

```bash
npm run typecheck
npm run build
```
