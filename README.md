# 🔌 **Análisis de Consumo Energético en el Hogar (2007–2010)**

**Autor:** Andrés Aranguren  
Proyecto personal de análisis de datos — 2025

Este proyecto analiza el consumo energético de un hogar utilizando el dataset _Household Power Consumption_.  
Incluye limpieza, transformación, análisis descriptivo, análisis temporal, estudio por sub-medición y conclusiones accionables.

---

## 📘 **Resumen Ejecutivo**

El consumo eléctrico del hogar está determinado principalmente por tres factores:

- ⏰ **Horarios pico:** 19:00–22:00
- ❄️ **Estacionalidad:** el invierno incrementa el consumo **+108%**
- 🔥 **Circuito dominante:** `Sub_metering_3` (calentador / calefacción)

Además:

- `Other_consumption` representa **≈70% del consumo total**
- Hay cargas fantasma activas incluso en madrugada
- Existen oportunidades claras de optimización energética

---

## 📂 **Estructura del Repositorio**

├── data/
│ └── household_power_consumption.csv
│
├── docs/
│ ├── HouseHold_Power_Consumption.html
│ └── HouseHold_Power_Consumption.pdf
│
├── images/
│ ├── analisis_descriptivo_general.png
│ ├── consumo_por_dia_semana.png
│ ├── consumo_por_estacion.png
│ ├── consumo_por_hora.png
│ ├── consumo_promedio_hora_dia_heatmap.png
│ ├── desglose_consumo_por_circuito.png
│ ├── evolucion_consumo_diario.png
│ ├── evolucion_consumo_mensual.png
│ └── patrones_consumo_electrico_diario.png
│
├── notebook/
│ └── HouseHold_Power_Consumption.ipynb
│
├── requirements.txt
└── README.md

---

# 🔍 **Etapas del Análisis**

## **1️⃣ Carga y Exploración Inicial**

- Previsualización del dataset
- Detección de valores nulos
- Análisis de tipos de datos
- Verificación de integridad temporal

---

## **2️⃣ Limpieza y Preparación**

- Conversión de columnas numéricas a `float64`
- Construcción de la columna `Datetime`
- Eliminación de **4069 filas nulas (0.39%)**
- Creación de la columna `Other_consumption`
- Resultado final: **1,044,506 registros limpios**

---

## **3️⃣ Análisis Descriptivo**

- Distribución de potencia activa
- Voltaje, intensidad y variabilidad
- Matriz de correlación
- Identificación de outliers reales por picos energéticos

---

## **4️⃣ Análisis Temporal**

- Consumo promedio por hora del día
- Consumo por día de la semana
- Consumo mensual y estacional
- Series temporales 2007–2010
- **Heatmap Hora × Día** para visualizar patrones combinados

---

## **5️⃣ Análisis por Sub-Medición**

Incluye:

- `Sub_metering_1` → Cocina
- `Sub_metering_2` → Lavandería
- `Sub_metering_3` → Calentador / calefacción
- `Other_consumption` → Restantes zonas del hogar

Se estudia:

- Circuito dominante
- Horas y meses de mayor consumo
- Comparación entre circuitos
- Detección de cargas fantasma

---

## 📊 **Resultados Destacados**

- 🔥 **Pico máximo diario a las 20:00**
- 📅 Fines de semana: **+25%** más consumo
- ❄️ Invierno: **+108%** más consumo que verano
- 🔌 `Sub_metering_3` es el principal consumidor energético
- ⚡ `Other_consumption` ≈ **70% del consumo total**
- 🌙 Consumo residual nocturno constante (cargas fantasma)

---

## 📈 **Visualizaciones Principales**

Incluye gráficos de:

- 🔥 Heatmap por hora y día
- ⏰ Consumo por hora
- 📅 Consumo por día de la semana
- 📉 Evolución mensual
- 🔌 Comparación de sub-mediciones
- 📈 Matriz de correlación

## Imágenes disponibles en: `images/`

# 📝 **Conclusiones Generales**

- El consumo del hogar está dominado por **patrones horarios y estacionales**.
- El **calentador/calefacción** es el mayor responsable energético.
- Existen consumos fantasma que pueden minimizarse.
- La franja más costosa es **19:00–22:00**.
- El mayor potencial de ahorro está en:
  - Optimizar el uso del calentador
  - Reducir standby
  - Desplazar usos intensivos a horarios no pico

---

# 🛠 **Instalación**

## 1. Clonar el repositorio

```bash
git clone https://github.com/TU_USUARIO/household-energy-analysis.git
cd household-energy-analysis
```

## 2. Crear entorno virtual (opcional pero recomendado)

```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate  # Windows
```

## 3. Instalar dependencias

```bash
pip install -r requirements.txt
```

## 4. Ejecutar el notebook

Abrir `notebook/HouseHold_Power_Consumption.ipynb` en Jupyter Notebook o JupyterLab.

```bash
jupyter notebook notebook/HouseHold_Power_Consumption.ipynb
# o
jupyter lab notebook/HouseHold_Power_Consumption.ipynb
```

# 👨‍💻Autor: Andrés Aranguren
