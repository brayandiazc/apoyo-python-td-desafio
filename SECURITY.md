# Política de Seguridad

Este documento describe cómo reportar problemas de seguridad en **Apoyo Desafios Bootcamp Python - TD** y qué prácticas seguimos en el repositorio.

> Nota: este repositorio contiene **material educativo** (ejemplos y apuntes de código). No es una aplicación desplegada ni expone servicios, por lo que la superficie de ataque es acotada. Aun así, agradecemos los reportes responsables.

## Tabla de Contenidos

- [Reporte de Vulnerabilidades](#reporte-de-vulnerabilidades)
  - [Información a incluir](#información-a-incluir)
  - [Qué esperar](#qué-esperar)
- [Versiones Soportadas](#versiones-soportadas)
- [Alcance](#alcance)
- [Fuera de Alcance](#fuera-de-alcance)
- [Manejo de Secretos](#manejo-de-secretos)
- [Contacto](#contacto)

## Reporte de Vulnerabilidades

Si descubres un problema de seguridad, **no abras un issue público**. Repórtalo de forma privada a través de uno de estos canales:

- **Email**: <brayandiazc@gmail.com> (preferido — usa un asunto que empiece con `Security:` para priorizarlo).
- **GitHub Security Advisories**: pestaña _Security_ del repositorio → _Report a vulnerability_.

### Información a incluir

Para poder triagear y responder rápido, incluye:

1. Descripción clara del problema.
2. Pasos para reproducirlo (PoC si es posible).
3. Impacto estimado.
4. Versión / commit afectado.
5. Sugerencia de mitigación (opcional).
6. Si quieres crédito público en la corrección, indica nombre y handle.

### Qué esperar

| Etapa                              | Tiempo objetivo             |
| ---------------------------------- | --------------------------- |
| Acuse de recibo                    | 48 horas hábiles            |
| Triage inicial y severidad         | 5 días hábiles              |
| Corrección                         | próxima actualización       |

Nos comprometemos a confirmar la recepción, mantenerte informado del progreso, no tomar represalias contra reportes de buena fe y acreditarte una vez publicada la corrección (si lo deseas).

## Versiones Soportadas

| Versión                 | Soporte de seguridad |
| ----------------------- | -------------------- |
| `main` (rama principal) | Sí                   |

## Alcance

Superficies **en alcance** para reportes:

- Código de ejemplo del repositorio que pudiera inducir a prácticas inseguras.
- Los flujos de GitHub Actions del repositorio (`.github/`), si se agregan.

## Fuera de Alcance

- Reportes de scanners automáticos sin impacto demostrado.
- Vulnerabilidades en dependencias de terceros sin vector de explotación en este material.
- Ingeniería social, phishing, DoS por volumen de tráfico.

## Manejo de Secretos

- **Nunca** commitear secretos en texto plano (claves de API, tokens, contraseñas, archivos `.env` con valores reales). El `.gitignore` ya excluye `.env` y archivos de claves.
- Si un secreto se commitea por error: **rota el secreto antes de limpiar la historia**. Reescribir la historia no es suficiente — asume que ya está comprometido.

## Contacto

- **Reportes de seguridad**: <brayandiazc@gmail.com> (asunto: `Security: …`)
- **Consultas generales**: <brayandiazc@gmail.com>

---

> Versión: 1.0 — Última actualización: 2026-07-02
