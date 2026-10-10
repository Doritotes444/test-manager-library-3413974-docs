# Manager Library Â· DocumentaciÃ³n TÃ©cnica y EspecificaciÃ³n SDD

> **Prueba TÃ©cnica de DesempeÃ±o SDD (Spec-Driven Development)**  
> **Servicio Nacional de Aprendizaje (SENA) Â· AnÃ¡lisis y Desarrollo de Software (ADSO) Â· Ficha 3413974**  
> **Desarrollador:** Juan Pablo Doria ([`@Doritotes444`](https://github.com/Doritotes444))  
> **Stack Implementado:** PHP 8.2 (Laravel 11) + React 18 (TypeScript + Vite) + PostgreSQL 16 / MySQL + Docker Compose  

---

## ðŸ“Œ Ãndice de Entregables de la DocumentaciÃ³n
* ðŸ‘‰ **[ENTREGA-TECNICA.md](ENTREGA-TECNICA.md)** â€” Informe tÃ©cnico maestro con diagramas Mermaid (Onion, Modelo ER, Secuencias de PrÃ©stamo y DevoluciÃ³n), matriz de trazabilidad y evidencias.
* ðŸ‘‰ **[spec-python/](spec-python/)** â€” EspecificaciÃ³n formal base para backend Python (de referencia).
* ðŸ‘‰ **[spec-.net/](spec-.net/)** â€” EspecificaciÃ³n formal base para backend .NET (de referencia).
* ðŸ‘‰ **[docs/ARCHITECTURE-ONION.md](docs/ARCHITECTURE-ONION.md)** â€” TraducciÃ³n de la arquitectura a **Onion Architecture pura** (4 capas concÃ©ntricas + Bootstrap).
* ðŸ‘‰ **[docs/adr/](docs/adr/)** â€” Registro de Decisiones de Arquitectura (ADR-001 a ADR-005).

---

## ðŸ›ï¸ Estructura del Ecosistema de 6 Repositorios

| Repositorio | Rol en la SoluciÃ³n | Enlace |
|---|---|---|
| **`test-manager-library-3413974-docs`** | EspecificaciÃ³n original, constituciÃ³n, ADRs y manual de entrega | [Doritotes444/test-manager-library-3413974-docs](https://github.com/Doritotes444/test-manager-library-3413974-docs) |
| **`test-manager-library-3413974-api`** | Backend REST en PHP 8.2 + Laravel 11 (Arquitectura Onion pura) | [Doritotes444/test-manager-library-3413974-api](https://github.com/Doritotes444/test-manager-library-3413974-api) |
| **`test-manager-library-3413974-app`** | Frontend SPA en React 18 + Vite + TypeScript (Nginx) | [Doritotes444/test-manager-library-3413974-app](https://github.com/Doritotes444/test-manager-library-3413974-app) |
| **`test-manager-library-3413974-infra`** | OrquestaciÃ³n Docker Compose, motor de base de datos y scripts de verificaciÃ³n | [Doritotes444/test-manager-library-3413974-infra](https://github.com/Doritotes444/test-manager-library-3413974-infra) |
| **`test-manager-library-3413974-page`** | Sitio pÃºblico estÃ¡tico de presentaciÃ³n responsivo (cero API) | [Doritotes444/test-manager-library-3413974-page](https://github.com/Doritotes444/test-manager-library-3413974-page) |
| **`test-manager-library-3413974-tool`** | Herramienta CLI de sembrado idempotente en Python vÃ­a HTTP | [Doritotes444/test-manager-library-3413974-tool](https://github.com/Doritotes444/test-manager-library-3413974-tool) |

---

## âš¡ EjecuciÃ³n RÃ¡pida del Sistema Completo

```bash
# 1. Clonar el repositorio de infraestructura (o el monorepo)
git clone https://github.com/Doritotes444/test-manager-library-3413974-infra.git infra
cd infra

# 2. Levantar los contenedores
docker compose up -d --build

# 3. Comprobar salud y ejecutar verificaciÃ³n de sondas
./verify.sh
```