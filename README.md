# 📡 TelecomX: Análisis de Fuga de Clientes (Churn Analysis)

![Python](https://img.shields.io/badge/Python-3.12-blue?style=for-the-badge&logo=python&logoColor=white)
![Manager](https://img.shields.io/badge/Package_Manager-uv-purple?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completado-success?style=for-the-badge)

## 📋 Descripción del Proyecto

Este proyecto simula un escenario real de **Ciencia de Datos** en el sector de las telecomunicaciones. El objetivo principal es analizar el ciclo de vida de los usuarios de **TelecomX** para identificar los factores determinantes en la **fuga de clientes (Churn)**.

El análisis abarca desde la ingesta de datos crudos complejos hasta la generación de estrategias de negocio para maximizar la retención.

## 🚀 Desafíos Técnicos y Soluciones

Este repositorio demuestra competencias avanzadas en Ingeniería de Datos y Análisis:

* **⚡ Gestión Moderna con `uv`:** Uso de `uv` para una gestión de dependencias ultrarrápida y reproducible, asegurando que el entorno sea idéntico en cualquier máquina (`uv.lock`).
* **🔄 ETL de Datos Anidados:** Los datos originales (JSON) presentaban una estructura anidada compleja. Se implementó un proceso de *flattening* (aplanamiento) para transformar diccionarios en variables tabulares útiles.
* **🧹 Limpieza de Alta Calidad:** Se logró un dataset con **0% de valores nulos** tras detectar y corregir datos vacíos ocultos y errores de tipado en variables financieras.
* **📊 Storytelling con Datos:** Traducción de hallazgos estadísticos en recomendaciones estratégicas claras.

## 📂 Estructura del Proyecto

```text
├── .venv/                   # Entorno virtual gestionado por uv
├── TelecomX_Data.json       # Dataset crudo (Fuente original)
├── TelecomX_diccionario.md  # Metadatos y descripción de variables
├── TelecomX_LATAM.ipynb     # Notebook principal (ETL + EDA + Insights)
├── pyproject.toml           # Definición de dependencias del proyecto
├── uv.lock                  # Archivo de bloqueo para reproducibilidad exacta
└── README.md                # Documentación del proyecto
```

## 📊 Insights Clave (Resultados)

El análisis exploratorio reveló 4 patrones críticos de comportamiento:

1.  🔴 **El Factor "Mes a Mes":** Los contratos mensuales son el predictor #1 de fuga. La fidelidad aumenta drásticamente en contratos anuales.
2.  📉 **La Zona de Peligro:** Los clientes con **menos de 12 meses** de antigüedad son los más vulnerables.
3.  ⚠️ **Paradoja de la Fibra Óptica:** A pesar de ser un servicio premium, presenta tasas de cancelación anormalmente altas (posible falla técnica o de precio).
4.  💸 **Fricción en Pagos:** El uso de *Electronic Check* está fuertemente correlacionado con el abandono.

## 💻 Instalación y Uso (Workflow con uv)

Este proyecto utiliza **uv** para garantizar la reproducibilidad exacta del entorno.

**1. Clonar el repositorio:**
```bash
git clone https://github.com/tu-usuario/telecomx-churn.git
cd telecomx-churn
```

**2. Sincronizar el entorno:**
Al tener el archivo `uv.lock`, solo necesitas un comando para instalar Python y todas las dependencias exactas:
```bash
uv sync
```

**3. Ejecutar el análisis:**
Puedes lanzar Jupyter Notebook utilizando el entorno gestionado por uv:
```bash
uv run jupyter notebook
```
*Si prefieres activar el entorno manualmente:*
```bash
source .venv/bin/activate  # Mac/Linux
.venv\Scripts\activate     # Windows
jupyter notebook
```

## 🛠️ Tecnologías Utilizadas

* **Python 3.12**
* **Pandas:** Manipulación y limpieza de datos (Wrangling).
* **Matplotlib & Seaborn:** Visualización de datos.
* **Requests:** Ingesta de datos vía API.
* **uv:** Gestión de dependencias y entornos virtuales.

---