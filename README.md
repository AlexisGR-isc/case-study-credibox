# 💳 Caso de Estudio — Plataforma de Gestión de Créditos

> **Nota de confidencialidad:** El código fuente de este proyecto no es público por acuerdo con el cliente. Este documento describe exclusivamente la arquitectura, decisiones técnicas e impacto medible del sistema.

---

## 🏛️ Contexto

| Campo | Detalle |
|---|---|
| **Empresa** | CrediBox |
| **Proyecto** | Plataforma de gestión de créditos comerciales |
| **Mi rol** | Desarrollador Full Stack |
| **Período** | Octubre 2022 – Febrero 2023 |
| **Clientes finales** | Banregio, Afirme |

---

## 🎯 Problema

La plataforma de gestión de créditos de CrediBox era comercializada a instituciones bancarias. Al incorporarme al proyecto, había dos frentes de trabajo simultáneos:

- **Nuevos módulos requeridos por el sector financiero:** los bancos clientes solicitaban funcionalidades específicas que debían integrarse sin romper la operación existente en producción
- **Deuda técnica en el frontend:** la versión original usaba Vue.js de forma directa, lo que generaba limitaciones de rendimiento y escalabilidad conforme la plataforma crecía

---

## ✅ Trabajo Realizado

- Desarrollo y mantenimiento de **APIs en Laravel** para los módulos de gestión de créditos
- Construcción de **interfaces en Vue.js** adaptadas a los requerimientos del sector financiero
- Administración y modificación de **base de datos en SQL Server** para la integración de nuevos módulos en producción
- Desarrollo de la **segunda versión del sistema**, migrando el frontend de Vue.js a Nuxt.js manteniendo la arquitectura basada en API

---

## 🏗️ Arquitectura

```
┌─────────────────────────────────────────────────┐
│           FRONTEND — Nuxt.js (v2)               │
│   Gestión de créditos · Módulos por banco       │
└───────────────────┬─────────────────────────────┘
                    │ API REST
┌───────────────────▼─────────────────────────────┐
│           BACKEND — Laravel                     │
│   Lógica de créditos · Módulos financieros      │
│   Validaciones · Reglas de negocio              │
└───────────────────┬─────────────────────────────┘
                    │
┌───────────────────▼─────────────────────────────┐
│         BASE DE DATOS — SQL Server              │
│   Créditos · Clientes · Transacciones           │
└─────────────────────────────────────────────────┘
```

---

## ⚙️ Decisiones de Arquitectura

**Migración Vue.js a Nuxt.js**
La segunda versión del sistema migró el frontend a Nuxt.js manteniendo la separación API/frontend intacta. La decisión buscaba mejorar rendimiento, escalabilidad y estructura del proyecto conforme la plataforma incorporaba más módulos y bancos clientes.

**Arquitectura basada en API**
El backend expone una API REST desacoplada del frontend. Esto permitió que la migración de Vue.js a Nuxt.js se realizara sin tocar la lógica de negocio del backend, y facilita incorporar nuevos clientes o canales en el futuro.

**SQL Server como base de datos**
La elección de SQL Server responde al entorno del sector financiero, donde es una tecnología estándar y ampliamente adoptada por las instituciones bancarias clientes.

---

## 🛠️ Stack Tecnológico

| Capa | Tecnología |
|---|---|
| Backend / API | Laravel (PHP) |
| Frontend v1 | Vue.js |
| Frontend v2 | Nuxt.js |
| Base de datos | SQL Server |

---

## 📊 Impacto

- Plataforma en producción operando con instituciones bancarias como Banregio y Afirme
- Segunda versión del sistema entregada con migración completa del frontend a Nuxt.js
- Nuevos módulos financieros integrados en producción sin afectar la operación existente

---

## 🔐 Nota de Confidencialidad

Este proyecto fue desarrollado bajo acuerdo de confidencialidad. El código fuente, los datos de clientes y los detalles internos del negocio no son públicos. Este caso de estudio documenta únicamente arquitectura, decisiones técnicas e impacto.

---

## 👤 Autor

**Alexis García Ruiz** — Desarrollador Full Stack

[![LinkedIn](https://img.shields.io/badge/LinkedIn-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/alexis-gr/)
[![GitHub](https://img.shields.io/badge/GitHub-AlexisGR--isc-black?style=flat&logo=github)](https://github.com/AlexisGR-isc)
[![Email](https://img.shields.io/badge/Email-isc.alexisgr@gmail.com-red?style=flat&logo=gmail)](mailto:isc.alexisgr@gmail.com)
