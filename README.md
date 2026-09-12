📊 Análisis Exploratorio de Datos: Salarios en Ciencia de Datos e IA

Este proyecto presenta un Análisis Exploratorio de Datos (EDA) sobre salarios de profesionales del área de Ciencia de Datos e Inteligencia Artificial, utilizando el dataset ds_salaries.csv.

El análisis fue desarrollado en R como parte de un taller de Estadística Descriptiva, aplicando medidas de tendencia central, dispersión, forma, frecuencias, cuantiles y diferentes visualizaciones.

Autor: David Mauricio Vargas Ramirez
Código: 824144

📌 Descripción del proyecto

El objetivo principal es explorar cómo se distribuyen los salarios y cómo estos varían de acuerdo con diferentes características de los trabajadores y las empresas.

El dataset contiene 607 registros correspondientes al periodo 2020–2022.

Las principales variables utilizadas en el análisis son:

experience_level: nivel de experiencia del trabajador.
company_size: tamaño de la empresa.
salary_in_usd: salario anual expresado en dólares estadounidenses.
remote_ratio: proporción de trabajo remoto.

Los niveles de experiencia analizados son:

Código	Nivel
EN	Entry Level
MI	Mid Level
SE	Senior Level
EX	Executive Level
🎯 Objetivos

El análisis busca:

Auditar y tipificar correctamente las variables del dataset.
Analizar la distribución de los registros según el tamaño de empresa.
Calcular medidas de tendencia central y dispersión de los salarios.
Comparar los salarios entre diferentes niveles de experiencia.
Analizar la asimetría y forma de las distribuciones.
Construir tablas de frecuencia por intervalos salariales.
Calcular cuantiles e identificar la distribución global de salarios.
Analizar qué proporción de perfiles EN alcanza un salario de $80,000 USD o más.
Presentar conclusiones descriptivas sobre los datos.
🛠️ Tecnologías utilizadas

El proyecto fue desarrollado utilizando:

R
R Markdown
LaTeX / XeLaTeX
ggplot2 — visualización de datos.
dplyr — manipulación de datos.
knitr — generación de tablas y documentos.
e1071 — cálculo de medidas estadísticas.
scales — formato de gráficos y valores.
📂 Estructura del proyecto
.
├── data/
│   └── ds_salaries.csv
│
├── analisis.Rmd
│
├── README.md
│
└── [PDF generado]


El nombre del archivo .Rmd puede variar dependiendo de la versión final utilizada para entregar el proyecto.

📈 Análisis realizado
1. Carga, auditoría y tipificación

Se realizó una revisión inicial de la estructura del dataset, identificando:

Número de registros y variables.
Tipos de datos.
Escalas de medición.
Valores faltantes (NA).
Registros duplicados.

Las variables categóricas fueron transformadas en factores ordenados cuando su naturaleza lo permitía.

2. Distribución por tamaño de empresa

Se construyó una tabla de frecuencias para company_size.

La distribución encontrada muestra un predominio de las empresas medianas:

M — Mediana: 326 registros (53.71%).
L — Grande: 32.62%.
S — Pequeña: 13.67%.

Esto significa que más de la mitad de los registros del dataset corresponden a trabajadores de empresas clasificadas como medianas.

3. Salarios según nivel de experiencia

Se calcularon diferentes estadísticos descriptivos para salary_in_usd agrupando por experience_level.

Entre las medidas utilizadas se encuentran:

Media.
Mediana.
# Análisis exploratorio de salarios en Ciencia de Datos e IA

Análisis exploratorio de datos (EDA) desarrollado en R para estudiar la distribución de salarios de profesionales de Ciencia de Datos e Inteligencia Artificial.

> Proyecto académico de Estadística Descriptiva · **Autor:** David Mauricio Vargas Ramirez · **Código:** 824144

## Descripción

El análisis utiliza `ds_salaries.csv`, un conjunto de **607 registros** correspondientes al periodo **2020–2022**. Se estudia cómo varía el salario anual según el nivel de experiencia y otras características de los trabajadores y las empresas.

Variables principales:

| Variable | Descripción |
| --- | --- |
| `experience_level` | Nivel de experiencia: EN, MI, SE o EX. |
| `company_size` | Tamaño de la empresa: pequeña, mediana o grande. |
| `salary_in_usd` | Salario anual expresado en dólares estadounidenses. |
| `remote_ratio` | Proporción de trabajo remoto: 0%, 50% o 100%. |

## Objetivos

- Auditar y tipificar las variables del conjunto de datos.
- Describir la distribución de los registros por tamaño de empresa.
- Calcular medidas de tendencia central, dispersión y forma.
- Comparar los salarios entre niveles de experiencia.
- Construir tablas de frecuencia, cuantiles y visualizaciones.
- Estimar qué proporción de perfiles `EN` alcanza al menos USD 80.000.

## Resultados destacados

- Las empresas medianas representan el **53,71%** de la muestra (326 registros).
- Los salarios tienden a aumentar a medida que crece el nivel de experiencia.
- La distribución salarial presenta asimetría positiva por la presencia de salarios altos.
- Aproximadamente el **31,8%** de los perfiles `EN` alcanza o supera los **USD 80.000**.
- El informe incluye medidas descriptivas por nivel de experiencia, tablas de frecuencia, boxplots, histograma y gráfico Q-Q.

Estos resultados describen únicamente la muestra analizada; no representan una estimación exacta del mercado laboral mundial.

## Estructura del proyecto

```text
.
├── README.md
└── primerTallerR/
    ├── data/
    │   └── ds_salaries.csv
    ├── primerTallerR.Rproj
    ├── taller_eda_salarios.Rmd
    └── taller_eda_salarios.pdf
```

## Tecnologías y paquetes

- [R](https://www.r-project.org/) y [R Markdown](https://rmarkdown.rstudio.com/)
- RStudio
- LaTeX con `xelatex` para generar el PDF
- `dplyr` y `ggplot2` para manipulación y visualización
- `knitr` para tablas y generación del informe
- `e1071` para medidas estadísticas
- `scales` para formatear valores y gráficos

## Cómo ejecutar el proyecto

### 1. Instalar los paquetes

Desde R:

```r
install.packages(c(
  "dplyr", "ggplot2", "knitr", "e1071", "scales", "rmarkdown"
))
```

También es necesario contar con una distribución de LaTeX compatible con `xelatex`.

### 2. Abrir el proyecto

Abre [primerTallerR/primerTallerR.Rproj](primerTallerR/primerTallerR.Rproj) en RStudio. El archivo CSV debe permanecer en [primerTallerR/data/ds_salaries.csv](primerTallerR/data/ds_salaries.csv).

### 3. Generar el informe

Abre [primerTallerR/taller_eda_salarios.Rmd](primerTallerR/taller_eda_salarios.Rmd) y selecciona **Knit** para generar el PDF. Desde la consola de R también puedes ejecutar:

```r
setwd("primerTallerR")
rmarkdown::render("taller_eda_salarios.Rmd")
```

## Contenido estadístico

El informe aplica conceptos de estadística descriptiva, variables cualitativas y cuantitativas, escalas de medición, frecuencias absolutas y relativas, media, mediana, desviación estándar, rango intercuartílico, coeficiente de variación, asimetría, cuartiles, percentiles, boxplots, histogramas y gráficos Q-Q.

## Limitaciones

- El conjunto de datos cubre únicamente el periodo 2020–2022.
- Los salarios dependen del país y no se ajustan por costo de vida.
- La composición de la muestra puede introducir sesgos y sobrerrepresentar algunas categorías.
- La asociación entre experiencia y salario no implica causalidad.