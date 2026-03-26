# Introducción

El presente análisis exploratorio de datos (EDA) se realiza sobre un conjunto de datos climáticos provenientes del reanálisis ERA5, desarrollado por el Copernicus Climate Change Service (C3S). Este dataset contiene información mensual para la región del Caribe durante el periodo comprendido entre 1976 y 2025, con una resolución espacial definida por una grilla de latitud y longitud.

Los datos están organizados en un formato multidimensional (NetCDF), lo que permite representar simultáneamente variaciones temporales y espaciales de diferentes variables atmosféricas y oceánicas. Entre las variables analizadas se incluyen temperatura del aire a 2 metros (t2m), temperatura superficial del mar (sst), presión a nivel del mar (msl), componentes del viento (u10, v10), precipitación total (tp) y diversos flujos de energía como radiación y calor latente.

Desde un punto de vista físico, es importante distinguir entre dos tipos de variables presentes en el dataset:

- **Variables de estado**: representan condiciones promedio del sistema climático en un instante o periodo determinado, como la temperatura, la presión o el viento. Estas variables dependen únicamente de las dimensiones de tiempo y espacio (latitud y longitud).

- **Variables de flujo o acumulación**: representan procesos que ocurren a lo largo del tiempo, como la precipitación, la radiación solar o los intercambios de energía entre la superficie y la atmósfera. Estas variables incluyen una dimensión adicional denominada `step`, que describe intervalos temporales dentro del periodo principal y permite capturar la acumulación o evolución de dichos procesos.

Esta distinción es fundamental para el análisis, ya que las variables de flujo requieren procesos adicionales de agregación (por ejemplo, sumas o promedios sobre la dimensión `step`) para ser interpretadas correctamente a escala mensual.

Este análisis constituye la base para estudios posteriores, tales como modelado climático, análisis de tendencias o desarrollo de modelos predictivos, garantizando que los datos utilizados sean confiables y coherentes desde el punto de vista físico y computacional.

