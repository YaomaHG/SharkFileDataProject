# SharkFileDataProject

Proyecto de la materia de Big Data para realizar un análisis exploratorio y
detectar patrones en incidentes por interacción con tiburones.

## Notebook

El análisis está implementado en
[`BigDataProject_OmarHG.ipynb`](./BigDataProject_OmarHG.ipynb) y puede abrirse
directamente en Google Colab:

[![Abrir en Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YaomaHG/SharkFileDataProject/blob/main/BigDataProject_OmarHG.ipynb)

## Flujo del análisis

El notebook:

1. Carga el dataset de incidentes desde `GSAF5.xls.csv`.
2. Limpia los nombres de columnas, elimina columnas auxiliares o vacías y
   descarta filas sin número de caso.
3. Normaliza la columna `Fatal (Y/N)` y crea la clasificación `Fatalidad`
   (`Fatal`, `No Fatal` o `Desconocido`).
4. Convierte `Year` y `Age` a valores numéricos y conserva los casos entre
   1900 y 2026.
5. Agrupa las actividades en `Surf / Deportes de tabla`, `Nado / Baño`,
   `Buceo / Snorkel`, `Pesca` y `Otras actividades`.
6. Genera visualizaciones sobre países con más incidentes, fatalidad,
   actividades y evolución por décadas.
7. Exporta el resultado limpio como `GSAF_limpio.csv`.

## Requisitos y ejecución

Se requiere Python con las siguientes librerías:

```bash
pip install pandas matplotlib seaborn
```

Para ejecutarlo localmente, coloca `GSAF5.xls.csv` en el directorio de trabajo,
abre el notebook y ejecuta sus celdas en orden. En Google Colab, sube el
dataset antes de ejecutar la celda de carga.

## Resultado

El archivo `GSAF_limpio.csv` contiene los casos modernos filtrados junto con
las columnas derivadas `Fatalidad`, `Actividad_Grupo` y `Decada`, que sirven
como base para el análisis exploratorio y las visualizaciones.
