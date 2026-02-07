Memo - Semana 4: Diseño Sistemático de Pruebas + Reglas de Oráculo

Fecha: 06/02/2026

Participantes:
- EVANS BALCAZAR VEIZAGA
- JORGE MARCELO ROSALES FUENTES
- MARCELO CORDERO FLORES
- SHIRLEY EULALIA PEREZ DELGADILLO

Objetivo de la semana: Diseñar pruebas sistemáticas para un punto concreto del SUT y definir oráculos defendibles (pass/fail), dejando evidencia reproducible y versionada en el repositorio.

Entregables obligatorios:
- design/oracle_rules.md (≥ 5 reglas de oráculo)
- design/test_cases.md (≥ 12 casos sistemáticos para 1 endpoint/función)
- scripts/systematic_cases.sh (ejecuta los casos y produce evidencia)
- evidence/week4/ (salidas por caso + RUNLOG.md)
- reports/week4_report.md (informe metodológico corto, 1–2 páginas)
- memos/week4_memo.md (memo semanal con formato del curso)

Actividades realizadas

Preparación y estructura del proyecto
Se creó la rama de trabajo week4 y se verificó la estructura de carpetas correspondiente: design/, scripts/, evidence/week4/, reports/, memos/.

La organización del repositorio se alineó con las prácticas establecidas, asegurando que todos los artefactos estuvieran correctamente versionados y documentados.

Selección del "objeto de prueba"
El equipo seleccionó el endpoint GET /pet/{id} como el objeto de prueba, debido a su alta variabilidad en los parámetros de entrada y su impacto potencial en la estabilidad y el rendimiento del sistema. Este endpoint fue considerado un buen candidato para aplicar un diseño sistemático de pruebas.

Definición del modelo de diseño sistemático
Se decidió aplicar la técnica de Equivalencia + Valores Límite (EQ/BV) para el diseño de los casos de prueba. Esta técnica se eligió porque permite cubrir un rango amplio de entradas sin generar combinaciones excesivas, lo que facilita una cobertura efectiva del sistema sin perder eficiencia.

Redacción de reglas de oráculo
Se definieron 5 reglas de oráculo vinculadas al endpoint seleccionado. Las reglas fueron estructuradas de la siguiente manera:
- Reglas mínimas: Oráculo "débil" que cubre casos básicos como la validación del código HTTP 200.
- Reglas estrictas: Oráculo "fuerte" que valida la estructura de la respuesta JSON y la consistencia de los datos.

Diseño de casos de prueba sistemáticos
Se diseñaron un total de 12 casos de prueba, siguiendo la técnica de EQ/BV. Cada caso cubre un conjunto de entradas representativas y sus resultados esperados se basan en las reglas de oráculo previamente definidas.

Los casos de prueba fueron organizados en el archivo design/test_cases.md, con cada caso claramente vinculado a las reglas de oráculo.

Implementación de ejecución reproducible
Se desarrolló el script scripts/systematic_cases.sh para ejecutar los 12 casos de prueba de manera automatizada. Este script es capaz de:

Ejecutar los casos definidos.
Aplicar las reglas de oráculo para determinar si la prueba pasó o falló.

Generar evidencia y guardarla en la carpeta evidence/week4/.
La ejecución del script se validó, asegurando su capacidad de ser ejecutado repetidamente por cualquier miembro del equipo.

Generación y versionado de evidencia
Se generaron archivos de evidencia en evidence/week4/, incluyendo salidas JSON de cada prueba y un resumen general de los resultados en summary.txt.

Además, se documentó el registro de ejecución en el archivo evidence/week4/RUNLOG.md, con fecha, hora, el comando exacto de ejecución, y el endpoint probado.

Informe metodológico
Se redactó el informe reports/week4_report.md, que incluye:
- Justificación de la selección del endpoint.
- Descripción de la técnica de diseño sistemático aplicada (EQ/BV) y sus ventajas.
- Explicación de cómo se definieron las reglas de oráculo (mínimas vs. estrictas).
- Identificación de las amenazas a la validez de las pruebas (internas, constructivas y externas).

Memo semanal
Se completó el memo memos/week4_memo.md con los logros de la semana, incluyendo la definición de oráculos, el diseño de los casos sistemáticos, la implementación de ejecución reproducible y la generación de evidencia, junto con los próximos pasos a seguir.

Resultados clave
- Oráculos definidos: 5 reglas de oráculo claras y reutilizables para evaluar las respuestas del endpoint.
- Casos sistemáticos diseñados: 12 casos de prueba basados en la técnica EQ/BV, documentados en design/test_cases.md.
- Ejecución reproducible implementada: El script scripts/systematic_cases.sh ejecuta las pruebas y produce evidencia consistente.
- Evidencia generada: Los resultados de las pruebas se almacenaron en evidence/week4/, con un registro completo en RUNLOG.md y resúmenes de los resultados.
- Informe metodológico: Se generó un informe detallado sobre el diseño y los límites de las pruebas realizadas.

Reflexión breve
Esta semana se enfocó en la importancia de un diseño de pruebas sistemático, lo que nos permitió generar evidencia de calidad y reproducible. La elección de un endpoint con alta variabilidad y la aplicación de técnicas como EQ/BV garantizó una cobertura efectiva del sistema sin caer en la trampa de pruebas ad-hoc. A través de las reglas de oráculo, pudimos establecer criterios claros para la validación de los resultados y facilitar la interpretación de los mismos. La ejecución automatizada con el script desarrollado también aporta un gran valor a la trazabilidad y la replicabilidad de las pruebas.

Próximos pasos
- Continuar con la ampliación de los casos de prueba para cubrir otros endpoints.
- Optimizar el script de ejecución para manejar más casos de prueba de manera eficiente.

Revisar y actualizar los oráculos en caso de detectar nuevas condiciones o resultados inesperados.
