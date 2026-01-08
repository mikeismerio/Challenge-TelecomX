# 📡 TelecomX: Análisis de Fuga de Clientes (Churn Analysis)

![Python](https://img.shields.io/badge/Python-3.12-blue?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas)
![Status](https://img.shields.io/badge/Status-Completado-success?style=for-the-badge)

## 📋 Descripción del Proyecto

Este proyecto aborda una problemática crítica en el sector de las telecomunicaciones: la **Retención de Clientes**. Utilizando un dataset de **TelecomX**, se desarrolló un flujo de trabajo de Ciencia de Datos para identificar patrones de comportamiento, limpiar datos complejos y predecir factores de riesgo asociados al abandono (*Churn*).

El proyecto simula un entorno real donde los datos provienen de fuentes externas (API/JSON) y requieren un preprocesamiento exhaustivo antes de ser analizados.

## 🚀 Características y Desafíos Técnicos

Este notebook no es solo un análisis exploratorio; incluye desafíos de ingeniería de datos resueltos:

* **ETL de JSON Anidado:** Los datos crudos contenían estructuras complejas (diccionarios dentro de columnas). Se implementó un proceso de *flattening* para tabularizar la información.
* **Limpieza de Datos Robusta:**
    * Detección y conversión de "valores ocultos" (espacios vacíos en variables numéricas).
    * Estandarización de tipos de datos (`object` -> `float`).
    * Traducción y normalización de columnas a `snake_case`.
* **Análisis Exploratorio (EDA):** Visualización de distribución de variables categóricas y numéricas para detectar correlaciones con la variable objetivo `Abandono`.

## 📊 Insights Clave (Resultados)

El análisis reveló que la fuga de clientes no es aleatoria. Los principales factores de riesgo detectados son:

1.  🔴 **Contratos Mensuales:** La inestabilidad contractual es el predictor #1 de fuga.
2.  📉 **La "Zona de Peligro":** Los clientes con menos de **12 meses** de antigüedad son los más vulnerables.
3.  ⚠️ **Fricción en Fibra Óptica:** A pesar de ser un servicio premium, presenta tasas de cancelación anormalmente altas.
4.  💸 **Métodos de Pago:** El uso de *Electronic Check* está fuertemente correlacionado con el abandono.

## 🛠️ Tecnologías Utilizadas

* **Python 3.12**
* **Pandas:** Manipulación y limpieza de datos.
* **Matplotlib & Seaborn:** Visualización de datos estadística.
* **Requests:** Ingesta de datos desde repositorios remotos.

## 💻 Instalación y Uso

Sigue estos pasos para ejecutar el proyecto en tu entorno local:

1.  **Clonar el repositorio:**
    ```bash
    git clone [https://github.com/tu-usuario/telecomx-churn.git](https://github.com/tu-usuario/telecomx-churn.git)
    cd telecomx-churn
    ```

2.  **Crear un entorno virtual (Recomendado):**
    ```bash
    # Usando venv
    python -m venv .venv
    source .venv/bin/activate  # En Windows: .venv\Scripts\activate
    
    # O usando uv (si lo tienes instalado)
    uv venv
    ```

3.  **Instalar dependencias:**
    ```bash
    pip install pandas matplotlib seaborn requests
    ```

4.  **Ejecutar el Notebook:**
    ```bash
    jupyter notebook TelecomX_LATAM.ipynb
    ```

## 📂 Estructura del Proyecto

```text
├── TelecomX_LATAM.ipynb   # Notebook principal con todo el análisis
├── README.md              # Documentación del proyecto
└── requirements.txt       # (Opcional) Lista de dependencias