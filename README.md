# Equipo-Clinia-Hackathon-Per-2026-
HealthSignal LATAM — RISA Data V1.0 Pipeline explicable de integración, detección híbrida y priorización de señales de riesgo Equipo Clinia — Hackathon Perú 2026 (Talento TECH)
Version 1
HealthSignal LATAM — RISA Data V1.
Pipeline explicable de integración, detección híbrida y priorización de señales de riesgo
Equipo Clinia — Hackathon Perú 2026 (Talento TECH)
Pregunta desafío (documento oficial):

¿Cómo diseñar una solución inteligente capaz de integrar información heterogénea de salud, analizar su evolución temporal y contextual, identificar y priorizar señales tempranas de riesgo y proporcionar evidencia explicable que apoye una toma de decisiones oportuna?

Cadena implementada: fuentes heterogéneas → integración e interoperabilidad → procesamiento y
contextualización → análisis temporal y multivariable → identificación de
patrones → valoración y priorización → explicabilidad y trazabilidad → apoyo
a la decisión — el flujo conceptual exacto del documento oficial del desafío.

Alcance de este notebook: catálogo completo de variables, integración multi-fuente, calidad de datos, features temporales, motor de detección híbrido (reglas duras + reglas de tendencia + scoring estadístico/ML), clasificación de patrones internos, priorización, consola interactiva in-notebook (cumple el requisito oficial de "interfaz, dashboard, API o consola" sin depender de Streamlit ni de un servidor externo — un notebook de Kaggle no sostiene una app persistente) y salida oficial (signals.csv/ evidence.csv) validada contra validate_submission.py.

Cómo está organizado
#	Sección	Qué responde
1	Rutas e ingesta cruda	Resolución robusta del dataset en Kaggle + carga de TODAS las tablas
2	Catálogo completo de variables	Qué contiene cada tabla, variable por variable, con gráficos
3	Interoperabilidad	Fuentes con distinta frecuencia/unidad/estructura, unidas por ID canónico
4	Catálogo de calidad	Cada fenómeno (missing, duplicados, outliers, unidades, frecuencia, desalineación, ruido, conectividad) con tratamiento justificado
5	Temporalidad	Ventanas, tendencias, combinaciones — ningún valor aislado define el caso
6	Motor híbrido	Reglas duras + reglas de tendencia + combinación multivariable + ML/SHAP
7	Alertas irrelevantes	Demostración de que el pipeline NO dispara en cada patrón engañoso conocido
8	Patrones internos RISA	Clasificador heurístico de NORMAL...COMPLEX (8 patrones)
9	Priorización	Agregación por episodio + recalibración por percentil
10	Salida oficial	signals.csv/evidence.csv con esquema exacto
11	Consola interactiva	Consulta in-notebook de cualquier señal (interfaz de apoyo a decisión)
12	Validación oficial	Corrida real de validate_submission.py
13	Síntesis	Respuesta explícita a la pregunta central del desafío
