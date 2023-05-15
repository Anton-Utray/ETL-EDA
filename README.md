# ETL-EDA

## Análisis exploratorio de datos (EDA)

### Índice

1. [✍️ Descripción](#descripcion)
2. [🎯 Objetivo](#objetivo)
3. [📊 Análisis](#analisis)
4. [💧 Conclusiones](#conclusion)
5. [Próximos pasos](#próximos)

### ✍️ Descripción<a name="descripcion"/>

Cuarto proyecto realizado dentro del Bootcamp de Data Analytics de IronHack.

Con este proyecto se propone la práctica de análisis tipo EDA. Para ello hemos tomado los archivos del proyecto ETL de la semana anterior [^1]

#### Pequeño recap ⏪ 👩‍🏫 

En este proyecto , habíamos extraido, transformado y subido a SQL 3 archivos:

- Ultímo censo de viviendas y hogares del INEGI que mapea por alcaldía la distribución de su población con acceso a agua corriente o en su defecto, las fuentes alternativas de abastecimiento. 

- Recopilación de proyectos de captura de agua en la CDMX, separado por alcaldias para el año 2022. 

- Indices de desarrollo por acladía.


#### Enriquecimiento 🧬 

Para enriquecer los datos de cara a la exploración de datos hemos realidazo lo siguiente:

- Añadir al archivo de proyectos de captura de agua de lluvia los datos para los años 2019, 2020 y 2021.

- Sacar el consumo de agua promedio por alcaldía. Extraído del portal del datos del Gobierno de la Ciudad de Mexico. 

### 🎯 Objetivo<a name="objetivo"/>

El objetivo de esta EDA es ir pintando una mejor imagen de la situación hidrica de las distintas alcaldías de la CDMX. 

Buscaremos despejar algunas de las siguientes icongnitas: 

- ¿Como se divide el acceso a agua por alcaldías?
- ¿Como se compara al indice de desarollo de cada sitio?
- En que partes de la ciudad ya se estan llevando a cabo proyectos de este tipo? 

### Análisis<a name="analisis"/>

#### Primer snapshot CDMX 

![DASH](https://github.com/Anton-Utray/ETL-EDA/blob/main/IMAGES/DASH%20acceso%20vs%20consumo.JPG)

#### Población vulnerable

![DASH](https://github.com/Anton-Utray/ETL-EDA/blob/main/IMAGES/Dash%20pob%20vulnerable.JPG)

#### Mapa proyectos de captura de agua (19-22)

![DASH](https://github.com/Anton-Utray/ETL-EDA/blob/main/IMAGES/Dash%20proyectos.JPG)

### Conclusiones<a name="conclusiones"/>

### Próximos pasos<a name="próximos"/>

Para poder concluir con nuestro mapeo, de cara al proyecto final del bootcamp tenemos los siguientes objetivos: 

- Bajar de esacala alcaldía a escala colonia y/o municipio. (Varios de nuestros archivos ya traen esta información pero incompleta, por restricciones de tiempo no hemos podido dedicar tiempo a esta parte)
- Continuar construyendo la base de datos en SQL.
- Agregar mapa de escuelas publicas. 

Footnotes:
[^1]: Proyecto ETL https://github.com/Anton-Utray/ETL
