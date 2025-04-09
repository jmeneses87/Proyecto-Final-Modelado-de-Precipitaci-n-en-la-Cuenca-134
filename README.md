# Proyecto Final – Modelado de Precipitación en la Cuenca 134

Este repositorio contiene el desarrollo completo del proyecto final para la asignatura **Análisis Predictivo**, donde se realizó un estudio de reconstrucción y predicción de la precipitación mensual en la Cuenca Hidrográfica del Río Grande (cuenca 134), ubicada en Panamá.

---

## 🗃 Estructura del Repositorio

- `/data/`  
  Contiene la base de datos cruda de precipitación ponderada por estación, el shapefile de la cuenca y los datos agregados mensuales por Thiessen.

- `/scripts/`  
  Contiene el script en RMarkdown (`PROYECTO_FINAL.Rmd`) con el flujo completo: carga de datos, limpieza, análisis descriptivo, modelado y predicción.

- `/resultados/`  
  Resultados del análisis, incluyendo el ranking de modelos evaluados y la predicción mensual de 2023.

---

## 📌 Datos Utilizados

- **Cuenca:** Cuenca Hidrográfica del Río Grande – Código 134
- **Estaciones utilizadas:**  
  RIO GRANDE, EL COPE, SONADORA, HUACAS DE QUIJE, RIO HONDO, PUERTO POSADA, LAS SABANAS, OLA
- **Período de análisis:** 1981–2022
- **Variable principal:** Precipitación diaria (ponderada por polígonos de Thiessen)
- **Archivos de datos:**
  - `estaciones.csv` – Estaciones Georeferenciadas
  - `precipitacion_cuenca134.csv` – Lluvia co datos faltantes
  - `lluvia_ponderada_estaciones.xlsx` – Datos procesados lluvia diaria
  - `cuenca134.shx` – Archivo de forma para el contorno de la cuenca 134
---

## 🧠 Modelos Utilizados

Se evaluaron y compararon los siguientes modelos de series de tiempo:

- Promedio Móvil (k=3)
- Suavizamiento Exponencial Simple (SES)
- Modelo de Holt
- Modelo de Holt-Winters (aditivo)
- Modelo de Holt-Winters (multiplicativo)
- Red Neuronal Autorregresiva (NNAR)

El modelo NNAR fue seleccionado como el mejor con base en su desempeño predictivo sobre datos del año 2021.

---

## 📈 Resultados Clave

- **Ranking de modelos:** Basado en MAD, MAPE, RMSE y otras métricas
- **Pronóstico mensual del año 2023:** Generado con NNAR y comparado con el promedio histórico (1981–2022)

---

## 👨‍🔬 Autor

**Joel Meneses**  
Estudiante de Maestría en Ingeniería con Énfasis en Recursos Hídricos  
Facultad de Ingeniería Civil – Universidad Tecnológica de Panamá

---

## 👨‍🏫 Profesor

**Juan Marcos Castillo, PhD**

---

## ⚠️ Créditos y Reconocimientos

- **Datos meteorológicos:** Instituto de Meteorología e Hidrología de Panamá (IMHPA)
- **Análisis y visualización:** Realizado en R y RStudio con paquetes como `forecast`, `tidyverse`, `lubridate`, y `nnetar`.

---

## 📅 Fecha de entrega

Abril 2025
