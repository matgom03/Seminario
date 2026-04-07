# Introducción

Este **análisis exploratorio de datos (EDA)** se realiza sobre un conjunto de datos climáticos provenientes del **reanálisis ERA5**, desarrollado por el **Copernicus Climate Change Service (C3S)**.

> **Contexto del dataset**  
> Información **mensual** para la región del **Caribe**, cubriendo el período **1976–2025**, con resolución espacial definida por una grilla de **latitud–longitud**.

---

## Estructura de los datos

Los datos se encuentran en formato **multidimensional (NetCDF)**, lo que permite analizar de manera conjunta la **variabilidad temporal y espacial** de múltiples variables atmosféricas y oceánicas.

###  Variables analizadas
- Temperatura del aire a 2 m (**t2m**)
- Temperatura superficial del mar (**sst**)
- Presión a nivel del mar (**msl**)
- Componentes del viento (**u10**, **v10**)
- Precipitación total (**tp**)
- Flujos de energía (radiación y calor latente)

---

##  Tipos de variables climáticas

Desde un punto de vista físico, es fundamental distinguir entre dos tipos de variables:

###  Variables de estado
Representan **condiciones promedio** del sistema climático en un instante o período determinado.

- Ejemplos: temperatura, presión, viento  
- Dependen solo de **tiempo, latitud y longitud**

### Variables de flujo o acumulación
Representan **procesos integrados en el tiempo**, como intercambios de energía o masa.

- Ejemplos: precipitación, radiación solar  
- Incluyen una dimensión adicional denominada **`step`**, que describe intervalos temporales internos

> **Nota metodológica**  
> Estas variables requieren **procesos adicionales de agregación** (sumas o promedios sobre `step`) para su correcta interpretación a escala mensual.

---

## Relevancia para el análisis

Esta distinción es **clave** para garantizar:
- Interpretaciones físicas correctas  
- Comparabilidad temporal  
- Aplicación adecuada de métodos estadísticos

