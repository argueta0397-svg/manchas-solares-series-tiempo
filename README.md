# Análisis del número medio mensual total de manchas solares mediante modelos de series temporales

**Autores:** Kevin Andrey Montenegro Barboza y Pamela Argueta Dimas
Escuela de Estadística, Universidad de Costa Rica

## Descripción

En este proyecto se comparan modelos de series temporales para describir y pronosticar el número medio mensual total de manchas solares, con datos de enero de 1749 a octubre de 2026. Se ajustaron modelos de cuatro familias:

- **Suavizamiento exponencial:** SES y Holt-Winters aditivo
- **ARIMA:** ARMA(1,1), ARMA(2,1) y ARMA(3,1)
- **Regresión:** términos de Fourier con las 5 frecuencias más altas del periodograma
- **Regresión dinámica:** términos de Fourier con errores ARMA(p,1)

Los finalistas de cada familia se compararon por su error de pronóstico en los últimos 132 meses (noviembre 2015 a octubre 2026). Con el modelo ganador se pronosticaron los siguientes 60 meses.

## Archivos

| Archivo | Contenido |
|---|---|
| `Proyecto_KevinM_Pamela.Rmd` | Código en R Markdown que genera el artículo |
| `Proyecto_KevinM_Pamela.pdf` | Artículo final |
| `data_final.xlsx` | Datos: año, mes y número medio mensual de manchas solares (3334 meses) |

## Datos

Los datos provienen de SILSO, del Solar Influences Data Analysis Center (Real Observatorio de Bélgica): <https://www.sidc.be/SILSO/datafiles>

## Cómo reproducir el análisis

1. Descargar o clonar el repositorio y dejar `data_final.xlsx` en la misma carpeta que el `.Rmd`.
2. Instalar los paquetes:

```r
install.packages(c("ggplot2", "forecast", "fpp2", "astsa", "car", "dplyr",
                   "readxl", "tseries", "knitr", "kableExtra"))
```

3. Abrir `Proyecto_KevinM_Pamela.Rmd` en RStudio y usar **Knit > Knit to PDF**. Hace falta una instalación de LaTeX, por ejemplo con `tinytex::install_tinytex()`.
