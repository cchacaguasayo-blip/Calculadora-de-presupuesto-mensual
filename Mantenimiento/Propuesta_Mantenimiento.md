# Propuesta de Mantenimiento — Calculadora de Presupuesto Mensual

## Resumen
Este documento propone un plan de mantenimiento para la Calculadora de Presupuesto Mensual. El objetivo es mantener la aplicación estable, corregir defectos críticos, y mejorar funcionalidad y experiencia de usuario mediante mejoras planificadas.

## Tipo de mantenimiento propuesto
- **Principal:** Mantenimiento **Perfectivo** — introducir mejoras funcionales y de usabilidad (gráficos, filtros, exportación, categorías personalizadas).
- **Complementario:** Mantenimiento **Correctivo** (corrección de errores) y **Adaptativo** (adaptación a nuevos navegadores o requisitos).

## Justificación
La versión inicial cumple funciones básicas (registro y cálculo). Para aumentar su utilidad se requieren mejoras (visualización por categoría, exportación, validaciones), por lo que el mantenimiento perfectivo agregará valor directo al usuario. Al mismo tiempo, hay que disponer procesos correctivos para errores y adaptativos para asegurar compatibilidad futura.

## Alcance del plan (6 meses — ejemplo)
### Mes 1 — Auditoría y correcciones críticas (Correctivo)
- Revisar funciones de cálculo y validaciones.
- Corregir errores detectados en sumas, guardado en localStorage y validaciones de entrada.
- Crear checklist de pruebas automatizables para funciones clave.

### Mes 2 — Mejoras UI/UX (Perfectivo)
- Rediseñar formularios (validaciones inline, mensajes claros).
- Implementar auto-complete para categorías frecuentes.
- Mejorar accesibilidad básica (labels, roles ARIA).

### Mes 3 — Dashboard y gráficos (Perfectivo)
- Añadir gráficos de distribución por categoría (pastel / barras).
- Implementar resumen mensual visual y listas ordenables.

### Mes 4 — Import/Export y backup (Perfectivo / Adaptativo)
- Exportar CSV y PDF del resumen mensual.
- Implementar importación básica de CSV con validación.
- Añadir opción de backup/restore en JSON.

### Mes 5 — Tests y documentación (Perfectivo)
- Escribir pruebas unitarias para funciones de cálculo.
- Documentar endpoints (si existieran) y estructura de datos en README.
- Crear guía de recuperación ante pérdida de datos.

### Mes 6 — Optimización y revisión (Adaptativo / Correctivo)
- Performance tuning para grandes volúmenes locales (hasta 10k transacciones).
- Pruebas de compatibilidad en navegadores y móviles.
- Revisiones finales y preparación de release.

## Procedimiento de gestión de incidencias
- **Clasificación por prioridad**
  - **P0 (Crítico):** Pérdida de datos, cálculos incorrectos. Acción inmediata: rollback a versión estable y parche urgente.
  - **P1 (Alta):** Funcionalidad principal afectada (ej. exportar fallando). Acción: parche en 72 h.
  - **P2 (Media):** Errores no críticos de UI. Acción: plan en próximo sprint.
- **Registro:** Cada incidencia se registra en el repositorio como *Issue* con pasos para reproducir, logs y capturas.
- **Responsable:** Asignar dueño del issue y fecha objetivo de resolución.
- **Comunicación:** Notas de release y changelog para cada parche o mejora.

## Métricas de éxito
- Tiempo medio de resolución de P0 < 24 h, P1 < 72 h.
- 0 pérdidas de datos reportadas en producción (local) tras 3 meses de despliegue.
- Cobertura de pruebas unitarias mínima para funciones de cálculo: 80%.
- Tiempo de recuperación de backup < 5 minutos (procedimiento verificado).

## Herramientas y prácticas recomendadas
- **Control de versiones:** GitHub — usar ramas `main`, `dev`, `feature/*`, `bugfix/*`.
- **Issues & Projects:** Usar GitHub Issues + Projects para priorizar y documentar tareas.
- **Commits:** Mensajes claros y pequeños; ejemplo: `fix: corregir cálculo de totales`, `feat: exportar CSV`.
- **Backups locales:** Exportar JSON periódicamente (manual o botón de backup).
- **Pruebas:** Crear pequeñas pruebas unitarias (scripts JS) para cálculo de totales y validaciones.
- **Documentación:** Mantener CHANGELOG.md y actualizar README con cambios importantes.

## Plan de releases y versionado
- Usar versionado semántico (SemVer): `v1.0.0`, `v1.1.0` (mejoras), `v1.1.1` (corrección menor).
- Preparar notas de release con resumen de cambios, instrucciones de migración y riesgos.

## Recomendaciones finales
- Automatizar al menos las pruebas básicas (funciones de cálculo) antes del despliegue de cada release.
- Mantener una política de commits y PRs: al menos una revisión por compañero antes de merge a `main`.
- Documentar claramente procedimientos de backup/restore en el repositorio (archivo `docs/backup_restore.md`).

