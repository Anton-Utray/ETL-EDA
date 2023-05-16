# AGUA y LLuvia en la CDMX

<p align="center">
  <img src="https://github.com/Anton-Utray/ETL-EDA/blob/main/IMAGES/tlaloc.jpg" alt="Tlaloc" width="500">
</p>

<p align="center">Tlaloc, dios azteca de la lluvia, agua y fertilidad</p>


## Análisis exploratorio de datos (EDA)

### Índice

1. [✍️ Descripción](#descripcion)
2. [🎯 Objetivo](#objetivo)
3. [📊 Análisis](#analisis)
4. [💧 Conclusiones](#conclusion)
5. [🏃🏽‍♀️ Próximos pasos](#próximos)

### ✍️ Descripción<a name="descripcion"/>

Cuarto proyecto realizado dentro del Bootcamp de Data Analytics de IronHack.

Con este proyecto se propone la práctica de análisis tipo EDA. Para ello hemos tomado los archivos del proyecto ETL de la semana anterior [^1]

<details>
<summary>Pequeño recap ⏪ 👩‍🏫</summary>
<br>

En este proyecto , habíamos extraido, transformado y subido a SQL 3 archivos:

- Ultímo censo de viviendas y hogares del INEGI de 2020 que mapea por alcaldía la distribución de su población con acceso a agua corriente o en su defecto, las fuentes alternativas de abastecimiento. 

- Recopilación de proyectos de captura de agua en la CDMX 2022, separado por alcaldias para el año 2022. 

- Indices de desarrollo por acladía 2020.
</details>

<details>
<summary>Enriquecimiento 🧬</summary>
<br>
 
Para enriquecer los datos de cara a la exploración de datos hemos realidazo lo siguiente:

- Añadir al archivo de proyectos de captura de agua de lluvia los datos para los años 2019, 2020 y 2021.

- Sacar el consumo de agua promedio por alcaldía. Extraído del portal del datos del Gobierno de la Ciudad de Mexico. 
</details>

### 🎯 Objetivo<a name="objetivo"/>

El objetivo de esta EDA es ir pintando una mejor imagen de la situación hidrica de las distintas alcaldías de la CDMX. Esta informarción informará la estrategia de la Coalición Tricolor con su proyecto piloto de instalación de sistemas de captura de agua en escuelas en la CDMX en situación de vulnerabilidad hidrica [^2]. 

Por lo tanto, con este EDA buscaremos despejar las siguientes icongnitas: 

- ¿Como se divide el acceso a agua por alcaldías?
- ¿Como se compara al indice de desarollo de cada sitio?
- ¿En que partes de la ciudad ya se estan llevando a cabo proyectos de este tipo? 

### 📊 Análisis<a name="analisis"/>

<details>
<summary>Primer snapshot CDMX</summary>
<br>

![DASH](https://github.com/Anton-Utray/ETL-EDA/blob/main/IMAGES/DASH%20acceso%20vs%20consumo.JPG)

A nivel total CDMX, alrededor del 96% de la población goza de acceso a agua corriente. Este numero varia entre alcaldías como Miguel Hidalgo donde el 99% de su población estan conectadas al servicio publico y otras como Milpa Alta donde el porcentaje se situa en 80%.

Sin embargo, como podemos apreciar en la tabla de consumo promedio por alcaldía, dicha cobertura no se refleja en una tasa de consumo equitativa. En gran parte esto se debe a que no todas las alcaldías gozan de un suministro continuo o de calidad apta para su consumo.

Finalmente, podemos observar una correlación directa entre indice de desarrollo de las alcaldías con respecto a su consumo promedio. 
</details>

<details>
<summary>Población vulnerable</summary>
<br>

![DASH](https://github.com/Anton-Utray/ETL-EDA/blob/main/IMAGES/Dash%20pob%20vulnerable.JPG)

En este Dashboard, agrupamos los totales de poblaciones en vulnerabilidad hidrica por alcaldía. 

Consideramos población susceptible de vulnerabilidad cuando no disponen de conexión al servicio publico de agua (independientemente de si el suministro es frecuente y/o de calidad)

Observamos que el total CDMX de población asciende a mas de 360mil personas y el 79% de estos se situan en tan solo 5 alcaldías. 

Estas 'top 5' alcaldías mas vulnerables cuentan todas con un indice de desarollo bajo o muy bajo, poniendo en relación este indice con el nivel de vulnerabilidad hidrica. 

Finalmente, haciendo *zoom* sobre las 5 alcaldías con mas población vulnerable, podemos apreciar que el camion cisterna predomina como fuente alternativa de abastecimiento.

En el caso de Xochimilco vemos que tienen proporción alta de personas que se abastecen gracias a llaves y pozos comunitarios. Al estar situada en una zona de humedales, nos hace sentido pero preocupa la contaminación notoria de los cuerpos de agua en esta alcaldía.  
</details>

<details>
<summary>Mapa proyectos de captura de agua (19-22)</summary>
<br>

![DASH](https://github.com/Anton-Utray/ETL-EDA/blob/main/IMAGES/Dash%20proyectos.JPG)

A primera vista podemos observar la aglomeración de proyectos al sur de la ciudad, en los limites de la zona urbana. Por estas zonas predomina el ambiente rural entre montañas y cerros, distinguibles en el mapa gracias a sus colores verdes y beige. 

En efecto, estas zonas son de las mas elevadas y remotas de la ciudad, por lo que tiene sentido instalar sistemas de captura de lluvia, ya que su topografia dificulta la infrastructura de tuberias. 

Aunuado a la orografía, podemos observar correlación entre el nivel de indice de desarrollo y el total de proyectos por alcaldía, donde gran parte se han efectuado en las alcaldías con los indices mas bajos.

De igual manera podemos hacer paralelo al Dashboard anterior: las top 5 alcaldías a nivel de proyectos cuinciden con las 5 alcaldías con mayor población en situación de vulnerabilidad hidrica. 

Sin embargo cabe destacar que Milpa Alta acapara una parte importante de los proyectos pero no es la alcaldía con mas población vulnerable. 

Tanto Tlalpan como Xochimilco podrían recibir mas apoyo de este tipo considerando la proporción de sus poblaciones vulnerables. 

 Entre 2021 y 2022 observamos un crecimiento exponencial de proyectos en la alcaldía de Milpa Alta y Tlalpan en menor medida. 

 Sin embargo, Xochimilco presencia un decrecimiento progresivo de numero de proyectos desde 2019 hasta 2022. 

 Tambien cabe mencionar no aparece en esta tabla Cuajimalpa de Morelos, que es la sexta alcaldía mas vulnerable en agregado poblacional vulnerable.

Finalmente, vemos que para la colonia La Magdalena Contreras se realizaron proyectos puntuales en el 2021 pero no se retomaron nuevas intalaciones en 2022. 
</details>

### 💧 Conclusiones<a name="conclusiones"/>

Este analisis exploratorio nos regala muchos *insights* sobre la geolocalicazión de la vulnerabilidad hidrica dentro de la CDMX, así como donde se estan centrando los esfuerzos para remediarlo, gracias a proyectos de captura de agua de lluvia. 

Observamos una correlación positiva entre las alcaldías mas vulnerables y los proyectos de instalación realizados a la fecha.

Determinamos areas de oportunidad en Xochimilco, Cuajimalpa de Morelos y La Magdalena Contreras.

Tambien mencionar que las alcaldías son nucleos poblacionales muy grandes y el indice de desarrollo se puede sesgar. Por lo tanto sería importante en un analisis futuro de bajar a nivel colonia o pueblo para sacar información mas pertinente y estrechar el numero de opciones. 

### 🏃🏽‍♀️ Próximos pasos<a name="próximos"/>

Para poder concluir con nuestro mapeo, de cara al proyecto final del bootcamp tenemos los siguientes objetivos: 

- Bajar de esacala alcaldía a escala colonia y/o municipio. (Varios de nuestros archivos ya traen esta información pero incompleta, por restricciones de tiempo no hemos podido dedicar tiempo a limpieza extensiva)
- Continuar construyendo la base de datos en SQL.
- Agregar mapa de escuelas publicas. 
- Añadir parametros adicionales de analisis como reportes de cortes de agua/tandeos, contaminación por zonas, precipitaciones...

Footnotes:
[^1]: Proyecto ETL https://github.com/Anton-Utray/ETL
[^2]: Proyecto Piloto captura de lluvia en escuelas de la Coalición: https://www.coalicion-tricolor.com/_files/ugd/441226_089487397102429a8db70da4a1a9c968.pdf 
