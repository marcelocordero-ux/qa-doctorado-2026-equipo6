# memos/week3_memo.md

## Memo - Semana 3: Estrategia Basada en Riesgos + Evidencia 

**Fecha**: 29 de enero de 2026 
- **Participantes:**
  - EVANS BALCAZAR VEIZAGA  
  - JORGE MARCELO ROSALES FUENTES  
  - MARCELO CORDERO FLORES  
  - SHIRLEY EULALIA PEREZ DELGADILLO   

**Objetivo de la semana:** Implementar estrategia de pruebas basada en riesgo + evidencia para la API Petstore.  
Priorizar control de calidad conectando: Riesgo → Escenario → Evidencia → Riesgo residual.  
Entregar artefactos obligatorios: risk_matrix.csv (≥8 riesgos, Top 3), test_strategy.md, evidence/week3/ + RUNLOG.md, week3_memo.md.

## Actividades realizadas
1. Entendimiento del proceso de gestión de riesgos
2. Preparación de rama y estructura de carpetas (risk/, evidence/week3/, memos/).
3. Definición de riesgos de calidad del producto (excluyendo gestión).
4. Construcción de matriz de riesgos (8 riesgos, scores 1–5, orden por score, Top 3: Disponibilidad, Latencia, Consistencia).
5. Mapeo de Top 3 riesgos a escenarios existentes de quality/scenarios.md (SC-01, SC-05, SC-06 + extensiones).
6. Redacción de estrategia mínima en risk/test_strategy.md (propósito, alcance, tabla Top 3, reglas de evidencia, residual, validez).

## Resultados clave
- Matriz completa con 8 riesgos, priorización clara y trazabilidad a escenarios Semana 2.
- Estrategia documentada y defendible (risk/test_strategy.md).
- Preparación para generar evidencia reproducible de los Top 3 (pendiente ejecución y documentación en evidence/week3/).

## Pendientes / Próximos pasos
- Ejecutar pruebas para Top 3 riesgos:
  - Smoke múltiple (R01 – Disponibilidad)
  - Mediciones de latencia baseline (R02 – SC-05)
  - Asserts de consistencia en respuestas (R03 – SC-06 extendido)
- Crear evidence/week3/RUNLOG.md con registro cronológico.
- Completar evidencias (logs, CSVs, JSON samples) y actualizar RUNLOG.
- Revisar y commitear todo antes de merge a main.

## Reflexión breve
La gestión de riesgos está ingresando a los procesos operativos organizacionales como un paradigma de aplicación, entre los aspectos discutidos en el grupo en la reunión estuvo definiendo que estándares de riesgos y aspectos de aplicabilidad existen en el mercado, de la cual se identificó las siguientes respuestas:
- Existen estandares y buenas prácticas como la ISO 31000 (Gestión de riesgos) que emite pasos, tares, responsables y objetivos de la gestión de riesgos.
- Desde un punto de vista aplicativo a los procesos actuales observamos que en normas como la generada por ASFI hace mención a las metodologías de auditoría basadas en riesgos.
Lo anterior descrito denota que las necesidades de implementar gestión de riesgos en las tareas operativas es un paradigma que apoya en centrar todos los recursos en los puntos más criticos que se vayan a determinar, por lo que la priorización en riesgos observables (disponibilidad, latencia, consistencia) permite generar valor rápido y evidencia defendible con bajo esfuerzo inicial.
El enfoque basado en escenarios existentes de Semana 2 facilita la trazabilidad y reutilización.

