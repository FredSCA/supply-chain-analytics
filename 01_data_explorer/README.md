
# 📦 Módulo 1: Data Explorer & Cleaner (Performance Almacén Tránsito)

Este módulo contiene el análisis exploratorio de datos (EDA) y la limpieza del registro histórico de despachos desde el almacén de tránsito (Dinet) hacia el almacén de mina.

## 🎯 Objetivo de Negocio

Evaluar la eficiencia operativa del almacén de tránsito respondiendo a tres preguntas clave:

1. ¿Cuál es el tiempo real de permanencia (Lead Time) del material?
2. ¿Cuál es la frecuencia de despachos por mes (estacionalidad)?
3. ¿Qué días de la semana representan el mayor pico de carga operativa?

## 🛠️ Hallazgos Principales

* **Lead Time:** El tiempo de tránsito validado es de **1 día (24 horas)**, lo que indica una alta eficiencia. Sin embargo, la falta de registro de horas exactas limita el análisis de variabilidad.
* **Calidad de Datos:** Se detectaron y depuraron **1,687 registros** con errores de digitación (fechas imposibles/negativas).
* **Estacionalidad:** Los meses de Septiembre, Octubre y Noviembre concentran los picos máximos de despacho (hasta 1,014 viajes en Octubre 2020).
* **Optimización:** Se realizó una selección de variables (Feature Selection), descartando columnas maestras para enfocar el análisis únicamente en los KPIs logísticos.

## 📂 Archivos

* `01_exploratory_analysis.ipynb`: Notebook con la limpieza, cálculo de KPIs y visualizaciones.
* *(Nota: El archivo Excel original no se incluye por políticas de privacidad y peso).*

## 🔍 Vista previa de los datos (Antes vs. Después)
Para demostrar el proceso de limpieza y selección de variables, se incluyen dos archivos con una muestra de 100 registros:
*   [`muestra_datos_crudos.csv`](./muestra_datos_crudos.csv): Extracto directo del Excel original (incluye columnas vacías, fórmulas y errores de digitación en fechas).
*   [`muestra_datos_limpios.csv`](./muestra_datos_limpios.csv): Extracto del dataset final, con variables seleccionadas, fechas validadas y registros anómalos eliminados.

*(El dataset original completo no se incluye por razones de privacidad y tamaño).*