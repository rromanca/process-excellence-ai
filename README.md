# Process Excellence AI

### Agente Inteligente de Mejora Continua y Optimización de Procesos

Proyecto desarrollado en el curso **Automatización Avanzada de Coderhouse**.

## Descripción

Process Excellence AI es un agente inteligente desarrollado con n8n y OpenAI, diseñado para asistir en el análisis preliminar de problemas operativos y administrativos.

El sistema interpreta consultas en lenguaje natural, identifica oportunidades de mejora continua y recomienda metodologías adecuadas utilizando un catálogo corporativo alojado en Google Sheets.

## Arquitectura

**Chat Trigger → AI Agent → Gmail**

El AI Agent dispone de dos conexiones nativas:

- **OpenAI Chat Model (GPT-4o):** interpretación de consultas y generación de recomendaciones.
- **Google Sheets Tool:** consulta autónoma del catálogo de metodologías.

Gmail registra automáticamente los resultados de los análisis para facilitar su supervisión.

## Metodologías disponibles

| Metodología | Aplicación |
|---|---|
| 5 Porqués | Análisis preliminar de causa raíz |
| Ishikawa | Identificación de causas potenciales |
| Pareto | Priorización de problemas |
| PDCA | Mejora continua iterativa |
| DMAIC | Resolución estructurada de problemas |
| 5S | Organización y estandarización |

## Características principales

- Agente de IA con System Prompt modular.
- Máximo de 6 iteraciones por ejecución.
- Invocación autónoma y contextual de herramientas.
- Consulta de Google Sheets en modo de solo lectura.
- Recomendaciones fundamentadas en metodologías de mejora continua.
- Restricciones operativas y escalamiento a responsables humanos.
- Registro automático de resultados mediante Gmail.

## Pruebas realizadas

**Prueba 1 — Fallas recurrentes:** el agente consultó Google Sheets y recomendó la metodología 5 Porqués.

**Prueba 2 — Saludo general:** el agente respondió sin ejecutar Google Sheets, demostrando selección contextual de herramientas.

**Prueba 3 — Reprocesos administrativos:** el agente recomendó Ishikawa y envió correctamente el análisis mediante Gmail.

## Tecnologías

- n8n Cloud
- OpenAI GPT-4o
- Google Sheets
- Gmail
- GitHub

## Configuración

Para reutilizar el workflow:

1. Importar el archivo JSON en n8n.
2. Configurar las credenciales correspondientes.
3. Vincular un catálogo de metodologías en Google Sheets.
4. Configurar el destinatario del registro por Gmail.
5. Ejecutar pruebas desde el Chat Trigger.

## Alcance

Este proyecto corresponde al **Checkpoint 1 — Configuración e Interfaces Agénticas**.

La arquitectura está diseñada para evolucionar en los próximos módulos incorporando sistemas multiagente, memoria, integraciones corporativas y recuperación aumentada por generación (RAG).

Las recomendaciones del agente son orientativas y requieren validación humana antes de implementar modificaciones en procesos reales.

---

**Autor:** Rodrigo Román Cassano  
**Formación:** Automatización Avanzada — Coderhouse
