# El consumo frutihortícola en Argentina (2009-2018) 🥦🍎

Esta investigacion analiza los patrones de consumo de frutas y verduras en la población adulta argentina en los años 2009, 2013 y 2018, y cómo estos se relacionan con variables socioeconómicas y territoriales, desde un enfoque *eco-epidemiológico*. Se basa en el análisis de datos relevados en la Encuesta Nacional de Factores de Riesgo (ENFR), entre otros relevamientos oficiales.

Se aplicaron Modelos Lineales Generalizados y Mixtos (GLMMs) simples, aditivos y complejos. Estos ultimos incluyeron combinaciones de interacciones entre sus variables, y de ellos se indentifico el modelo con  mejor ajuste explicativo.

## Objetivo

Estudiar como el cumplimiento del consumo mínimo recomendado por la OMS (400g diarios) está asociado y determinado por factores como:
- Nivel socioeconómico a nivel individual, hogar y provincial
- Género
- Cantidad de hectareas implantadas (EAP frutihortícolas) segun jurisdiccion

## Bases de datos 🗃️

- Encuesta Nacional de Factores de Riesgo (ENFR 2009, 2013, 2018)
- Censo Nacional (2010) – Necesidades Básicas Insatisfechas (NBI)
- Censo Nacional Agropecuario – Superficie cultivada frutihortícola (2008, 2018)

## Herramientas y paquetes 🧠

- `R` y `R Markdown`
- `tidyverse` (manipulación de datos y visualizaciones)
- `glmmTMB` (modelado estadístico)
- `DHARMa`, `emmeans` (validación de modelos y estimación marginal)

## Análisis y resultados 📊

- Se modeló el cumplimiento con GLMMs de distribución binomial.
- Se identificaron desigualdades sociales: las personas de mayor ingreso, mayor nivel educativo y sin carencias estructurales de la vivienda tienen más probabilidades de cumplir con la recomendación.
- Las desigualdades, entre las personas de mayor y menor ingreso, crecieron entre 2009 y 2018.
- Las mujeres presentaron mayor cumplimiento que los varones en todos los años.
- No se halló relación significativa con el NBI provincial.
- La superficie frutihortícola mostró una relación contraria a lo esperado, probablemente por limitaciones en la variable.

### Mapa de probabilidades estimadas

![Mapa probabilidades estimadas](./resultados/Media_de_probabillidad_estimada_del_CFyV_para_cada_provincia.png)

> **Figura:** Probabilidad estimada, a partir del modelo seleccionado, de cumplimiento del consumo mínimo recomendado de frutas y verduras en un día típico, según provincia. Los valores fueron obtenidos mediante predicción marginal ajustada (`emmeans`) y representan diferencias territoriales luego de controlar por otras variables sociodemográficas.



## Archivos 📁


- [`informe_tesis.html`](./informe/Resumen_tesis.html): Informe interactivo en HTML (no visible en GitHub, requiere descarga)
- [`informe_tesis.pdf`](./informe/Resumene_tesis.pdf): Informe completo en PDF listo para lectura
- `procesamiento_datos.Rmd`: Limpieza, recodificación y armado de las bases (en preparación)

---

> 📌 Este proyecto nace de mostrar y compartir los resultados de mi tesis de grado en Ciencias Biológicas por la universidad de Buenos Aires (Fcen)(orientación en Salud Pública y Bioestadística) y representa mis primeros pasos en la transición profesional hacia el análisis de datos aplicado a problemas sociales y de salud.
