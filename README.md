# Análisis de Ventas — Alura Store Latam (Challenge Data Science)

Este repositorio contiene un análisis exploratorio de ventas para cuatro tiendas (Tienda 1 a Tienda 4) usando datos públicos del challenge de Alura Latam. El objetivo es comparar el rendimiento de cada tienda y apoyar una recomendación final basada en métricas de negocio y satisfacción del cliente.

## Contenido del proyecto

- **Notebook principal (`.ipynb`)**
  - Carga de datos desde URLs (CSV de las 4 tiendas).
  - Limpieza y validación de variables numéricas (Precio, Calificación, Costo de envío, lat, lon).
  - Cálculo de métricas clave por tienda:
    - **Ingresos totales** (suma de `Precio`).
    - **Cantidad de ventas por categoría** (Top 5 por tienda).
    - **Calificación promedio** de clientes por tienda.
    - **Productos más vendidos y menos vendidos** por tienda (tablas separadas).
    - **Costo de envío promedio** por tienda (considerando que lo paga el cliente).
  - **Visualizaciones (Matplotlib)** para interpretar los resultados:
    - Barra: ingresos por tienda.
    - Barras agrupadas: Top 5 categorías más vendidas (comparación por tienda).
    - Dispersión: relación entre costo de envío promedio y calificación promedio.
    - Barra: productos más vendidos (Top N global y/o por tienda).
  - **Análisis geográfico (lat/lon)**
    - Dispersión (scatter) de ventas por tienda.
    - Mapa de calor (hexbin) para identificar concentración de ventas.
    - (Opcional) Mapas interactivos con Folium (heatmaps).
    - Comparación de desempeño por zonas (grilla lat/lon) para detectar patrones regionales.

## Dataset

Los datos se cargan directamente desde GitHub (Alura Latam), para las 4 tiendas:
- `tienda_1.csv`
- `tienda_2.csv`
- `tienda_3.csv`
- `tienda_4.csv`

Columnas principales:
- `Producto`, `Categoría del Producto`, `Precio`, `Costo de envío`, `Fecha de Compra`,
  `Vendedor`, `Lugar de Compra`, `Calificación`, `Método de pago`, `Cantidad de cuotas`,
  `lat`, `lon`.

## Requisitos

- Python 3.x
- Librerías:
  - `pandas`
  - `matplotlib`
  - (opcional) `folium`

## Cómo ejecutar

1. Abrir el notebook en **Google Colab** o Jupyter.
2. Ejecutar las celdas en orden:
   - Carga de datos
   - Análisis por tienda
   - Visualizaciones
   - (Opcional) análisis geográfico con mapas

## Resultados esperados

Al finalizar, el notebook entrega:
- Tablas comparativas por tienda (ingresos, satisfacción, costos de envío).
- Rankings de categorías y productos más/menos vendidos.
- Gráficos que facilitan la interpretación del desempeño.
- Análisis geográfico para detectar zonas con mayor concentración de ventas.

## Autor

Randy Roco  
Challenge Data Science — Alura Latam
