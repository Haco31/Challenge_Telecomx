# **CHALLENGE_CIENCIA_DE_DATOS_TELECOMX.**
# Proyecto de Análisis de Evasión de Clientes en TelecomX

Este proyecto se enfoca en el análisis de datos para comprender y abordar el problema de la evasión de clientes (Churn) en la empresa de telecomunicaciones TelecomX. El objetivo principal es identificar los factores que contribuyen a que los clientes cancelen sus servicios y proponer estrategias para mejorar la retención.

## Contenido

- [Descripción del Proyecto](#descripción-del-proyecto)
- [Fuentes de Datos](#fuentes-de-datos)
- [Preprocesamiento de Datos](#preprocesamiento-de-datos)
- [Análisis Exploratorio de Datos (EDA)](#análisis-exploratorio-de-datos-eda)
- [Resultados y Conclusiones](#resultados-y-conclusiones)
- [Recomendaciones](#recomendaciones)
- [Tecnologías Utilizadas](#tecnologías-utilizadas)
- [Cómo Ejecutar el Código](#cómo-ejecutar-el-código)

## Descripción del Proyecto

La evasión de clientes es un desafío significativo para las empresas de telecomunicaciones. Este proyecto aborda este problema mediante la exploración de datos de clientes de TelecomX para:

- Limpiar y transformar datos de clientes.
- Identificar patrones y características de clientes que tienden a cancelar sus servicios.
- Visualizar la relación entre diversas variables y la tasa de Churn.
- Proporcionar insights y recomendaciones para estrategias de retención de clientes.

## Fuentes de Datos

Los datos utilizados en este proyecto provienen de un archivo JSON alojado en un repositorio de GitHub:

- **URL:** `https://raw.githubusercontent.com/alura-cursos/challenge2-data-science-LATAM/refs/heads/main/TelecomX_Data.json`

## Preprocesamiento de Datos

El código realiza las siguientes operaciones de preprocesamiento:

- **Carga de Datos:** Se carga el archivo JSON en un DataFrame de Pandas.
- **Normalización de Datos Anidados:** Se extrae y normaliza la información de las columnas anidadas (`customer`, `phone`, `internet`, `account`).
- **Combinación de Datos:** Los datos normalizados se combinan con el DataFrame principal.
- **Eliminación de Columnas Originales:** Se eliminan las columnas anidadas originales.
- **Manejo de Valores Numéricos:** La columna 'Charges.Total' se convierte a tipo numérico, manejando errores y asegurando el tipo de dato float64.
- **Estandarización de Texto:** Se limpian y estandarizan valores en columnas como 'Contract' y 'MultipleLines'.
- **Creación de Nuevas Variables:** Se crea la columna 'Cuentas.Diarias' basada en 'Charges.Monthly'.

## Análisis Exploratorio de Datos (EDA)

El análisis exploratorio incluye:

- **Estadísticas Descriptivas:** Se obtienen estadísticas resumen para las variables numéricas.
- **Distribución de Variables Categóricas:** Se visualiza la distribución de clientes por 'gender', 'Contract' y 'PaymentMethod' utilizando gráficos de barras.
- **Análisis de Variables Numéricas y Evasión:** Se explora la relación entre 'Charges.Total' y 'Churn' mediante gráficos de densidad (kdeplot) y boxplots.

## Resultados y Conclusiones

Los hallazgos clave del análisis se detallan en el notebook, pero algunas conclusiones importantes incluyen:

- La cantidad de contratos 'Mes a Mes' es significativamente alta y estos clientes muestran una mayor propensión a cancelar.
- Se observa una relación entre el 'Total Gastado' y el comportamiento de cancelación.

## Recomendaciones

Basado en los resultados del análisis, se proponen recomendaciones para reducir la tasa de Churn, como:

- Implementar programas de fidelización para clientes con bajo gasto o contratos cortos.
- Investigar las causas de la alta evasión en segmentos de clientes específicos (ej. ciertos métodos de pago o tipos de contrato).
- Promocionar servicios adicionales asociados a una menor tasa de evasión.

## Tecnologías Utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn

## Cómo Ejecutar el Código

1.  Clona o descarga el repositorio que contiene el notebook.
2.  Abre el notebook en Google Colab o un entorno Jupyter.
3.  Asegúrate de tener instaladas las bibliotecas necesarias (`pandas`, `numpy`, `matplotlib`, `seaborn`). Puedes instalarlas si es necesario utilizando `!pip install <nombre_biblioteca>` en una celda de código.
4.  Ejecuta las celdas del notebook secuencialmente para cargar los datos, realizar el preprocesamiento, el análisis exploratorio y visualizar los resultados.
