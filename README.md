<!-- TABLA DE CONTENIDO -->
<details>
  <summary>Tabla de contenido</summary>
  <ol>  
    <li><a href="#Introducción">Introducción</a></li>
    <li><a href="#Objetivo">Objetivo</a></li>
    <li><a href="#ámbito-de-proyecto">Ámbito de Proyecto</a></li>
    <li><a href="#ETL">ETL</a></li>
    <li><a href="EDA">EDA</a></li>
    <li><a href="#Kpis">KPIS</a></li>
  </ol>
</details>


## Introducción

En la Ciudad de Buenos Aires, la seguridad vial es un tema de preocupación constante. Los siniestros viales, lamentablemente, son eventos frecuentes que afectan la vida de sus residentes y visitantes. Cada año, miles de personas son víctimas de accidentes de tráfico, algunos de los cuales resultan en lesiones graves o incluso en tragedias fatales. La magnitud de este problema no solo impacta en la salud y seguridad de las personas, sino que también afecta la infraestructura vial y los servicios de emergencia.

En este contexto, surge nuestro proyecto individual, una iniciativa que busca utilizar el poder de los datos y el análisis para abordar el desafío de los siniestros viales en la Ciudad de Buenos Aires. En colaboración con el Observatorio de Movilidad y Seguridad Vial (OMSV), nos hemos propuesto la tarea de analizar a fondo los incidentes de tráfico ocurridos en los últimos años. Nuestro objetivo es claro: generar información valiosa que permita a las autoridades locales tomar medidas efectivas para reducir la cantidad de víctimas fatales en estos incidentes.

Este proyecto no solo es una oportunidad para aplicar nuestras habilidades de análisis de datos, sino también un compromiso con la seguridad y el bienestar de la comunidad. A través de este informe, te invitamos a explorar nuestro enfoque y descubrir cómo los datos pueden desempeñar un papel fundamental en la construcción de una ciudad más segura en las carreteras de Buenos Aires.
---

Puedes personalizar esta introducción según las especificaciones y detalles específicos de tu proyecto.

***¡Disfruta del recorrido!***

## Objetivo

El objetivo del proyecto "Siniestros Viales" es abordar el problema de los accidentes de tráfico o siniestros viales en la Ciudad de Buenos Aires desde la perspectiva de un Data Analyst. El proyecto tiene como contexto el alto volumen de tráfico y la densidad poblacional en la ciudad, lo que aumenta la preocupación por la seguridad vial.

El rol a desarrollar en este proyecto implica colaborar con el Observatorio de Movilidad y Seguridad Vial (OMSV) bajo la órbita de la Secretaría de Transporte del Gobierno de la Ciudad Autónoma de Buenos Aires. El objetivo principal es analizar un conjunto de datos sobre homicidios en siniestros viales ocurridos en la Ciudad de Buenos Aires durante el período 2016-2021. A partir de este análisis, se busca generar información que permita a las autoridades locales tomar medidas efectivas para reducir la cantidad de víctimas fatales en siniestros viales.

El proyecto se divide en varias etapas, que incluyen un Análisis Exploratorio de Datos (EDA), la creación de un Dashboard interactivo, la medición y representación de KPIs relacionados con la seguridad vial, y la creación de un repositorio en GitHub que incluye un informe de análisis basado en los dashboards y los KPIs.

En resumen, el objetivo principal del proyecto es utilizar el análisis de datos para contribuir a la reducción de la cantidad de víctimas fatales en siniestros viales en la Ciudad de Buenos Aires, brindando información valiosa a las autoridades para la toma de decisiones en materia de seguridad vial.

## Ámbito de Proyecto

El proyecto se desarrolló siguiendo estos aspectos clave:
- Análisis exploratorio de datos y Preprocesamiento de datos: [EDA y ETL link](https://github.com/Yuliedpardo/PI_DA/blob/main/EDA_homicidios.ipynb)
- Desarrollo KPIS: [Desarrollo de los KPIS link](https://github.com/Yuliedpardo/PI_DA/blob/main/KPIS.ipynb)

</br>

## Pila de Tecnologías

![Visual Studio Code](https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white)
![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)
![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)
![Markdown](https://img.shields.io/badge/markdown-%23000000.svg?style=for-the-badge&logo=markdown&logoColor=white)


## ETL

Durante la fase de transformación y limpieza de datos (ETL), se han aplicado una serie de pasos esenciales para garantizar la calidad y coherencia de los datos. Estas acciones buscan preparar el conjunto de datos de manera óptima para su análisis posterior y para ser consumido por la API que se está desarrollando.

**1. Eliminación de Duplicados y verificamos tipo de datos por cada tabla :** Para asegurar la unicidad de las filas en el conjunto de datos, se han eliminado los duplicados y verificando tipos de datos para cada tabla.

**2. Filtrado de Fechas Inválidas:** Se ha realizado un filtrado riguroso en la columna 'release_date' para identificar y cuantificar los valores atípicos que no cumplen con el formato aaaa-mm-dd. Esto proporciona una comprensión clara de la calidad de los datos y posibles problemas en las fechas de lanzamiento.

**3. Union de las tablas:** Como parte de la transformación se ha realizado la union de las tablas por medio de un inner para que se traiga la informacion completa y se pueda trabajar de manera mas optima.

**4. Gestión de Valores Nulos:** Dado que los valores nulos en la columna "year_release" podrían afectar negativamente el funcionamiento de la API, se han eliminado de manera consciente. Esto garantiza que solo se consideren registros con años válidos al llamar a la API, previniendo resultados inesperados y errores en el procesamiento de datos.

**5. Identificación de Outliers:** Para asegurar la integridad de la columna "year_release", se ha revisado cuidadosamente mediante la ordenación y filtrado de los primeros y últimos valores. Esta inspección visual permite identificar posibles outliers o valores incoherentes que podrían requerir tratamiento adicional para su corrección o eliminación.

**6. Eliminación de Registros Incoherentes:** La eliminación de registros incoherentes es una medida importante para mantener la calidad de los datos. En caso de encontrar registros con valores nulos en todas las columnas relevantes para la API, se ha procedido a eliminarlos. Esto asegura que los análisis futuros se basen en datos confiables y coherentes.

**7. Creacion de nuevas columnas:** se crearon dos columnas nuevas llamadas semtestre y rango etario todo esto con el fin de poder realizar el kpis y un dashboard mas claro.


*Todas estas etapas se llevaron a cabo de manera local en **Visual Studio Code (VSCODE)**, empleando **Jupyter Notebook** como nuestro entorno principal. Para la implementación de cada paso, contamos con la potencia de **Python** como lenguaje de programación, respaldado por las versátiles bibliotecas **numpy y pandas**, que fueron fundamentales para la manipulación y transformación eficiente de los datos. Estas herramientas esenciales se combinaron hábilmente para crear un flujo de trabajo fluido y eficaz, permitiendo que el proyecto tomara forma de manera coherente y organizada.*

## EDA

Utilizando los datos resultantes del proceso ETL, se llevó a cabo un análisis exploratorio de datos (EDA) que desveló fascinantes perspectivas y patrones subyacentes. Para potenciar este análisis, se empleó la herramienta ProfileReport de la librería ydata_profiling, que permitió una inspección exhaustiva de todas las columnas. Este proceso enriquecedor no solo iluminó las características fundamentales de los datos, sino que también ofreció una visión detallada de cómo abordar cuestiones como valores faltantes, valores atípicos y mucho más.

acontinuacion haremos un analisis exahustivo por categoria 

**1. Relación entre AÑO y el Número de Víctimas :**

![Relación entre AÑO y el Número de Víctimas](https://github.com/Yuliedpardo/PI_DA/blob/main/imagenes/RELACION_A%C3%91O_VICTIMAS.png)

Analisis grafica 1 : 

1. Tendencia temporal:
   Observamos que el cuadro presenta datos desde 2016 hasta 2021. Esto nos permite analizar la tendencia temporal en el número de víctimas. Podemos notar una disminución en el número de víctimas desde 2018 hasta 2021 después de un pico en 2018.

2. Pico en 2018:
   El año 2018 destaca como el año con el mayor número de víctimas, con 149. Sería interesante investigar por qué hubo un aumento significativo en ese año en comparación con años anteriores y posteriores.

3. Disminución en 2019 y 2020:
   En 2019, el número de víctimas disminuyó a 104, y en 2020 disminuyó aún más a 81. Esto podría indicar una tendencia a la baja en la cantidad de víctimas durante estos dos años.

4. Aumento en 2021:
   Sin embargo, en 2021, el número de víctimas aumentó nuevamente a 97. Sería interesante investigar las razones detrás de esta reversión en la tendencia a la baja después de dos años de disminución.

5. Posibles factores influyentes:
   Para un análisis más completo, sería útil considerar posibles factores que podrían haber contribuido a las variaciones en el número de víctimas a lo largo de estos años. Algunos factores que podrían influir incluyen políticas gubernamentales, cambios en la economía, medidas de seguridad, entre otros.

6. Estadísticas descriptivas:
   Sería útil calcular estadísticas descriptivas como la media, la mediana y la desviación estándar para tener una idea más precisa de la distribución de los datos y la variabilidad en el número de víctimas a lo largo de estos años.

**2. Número de Víctimas por Comuna :**

![Número de Víctimas por Comuna](https://github.com/Yuliedpardo/PI_DA/blob/main/imagenes/victimas_por_comuna.png)


1. Distribución de víctimas por comuna:
   - La tabla muestra 16 comunas diferentes (números del 0 al 15) y el número de víctimas en cada una de ellas.
   - La cantidad de víctimas varía significativamente entre las comunas, oscilando entre 2 y 93 víctimas.

2. Comuna con el mayor número de víctimas:
   - La comuna con el mayor número de víctimas es la Comuna 1, con 93 víctimas. Esto podría indicar un área de interés para investigar más a fondo las razones detrás de esta cifra alta.

3. Comuna con el menor número de víctimas:
   - La Comuna 0 tiene el menor número de víctimas, con solo 2. Esto también puede ser un punto de interés para investigar las condiciones que llevan a esta cifra baja.

4. Distribución general:
   - La distribución de víctimas en estas comunas parece ser bastante heterogénea, ya que algunas comunas tienen un número significativamente mayor de víctimas que otras.

5. Análisis estadístico:
   - Sería útil realizar un análisis estadístico más detallado para comprender mejor la variabilidad en el número de víctimas entre las comunas. Esto podría incluir cálculos como la media, mediana, desviación estándar y otros estadísticos descriptivos.

6. Factores influyentes:
   - Para un análisis más completo, sería importante considerar factores que podrían influir en el número de víctimas en cada comuna. Estos factores podrían incluir la densidad de población, la presencia de servicios de seguridad, medidas de prevención del delito, entre otros.

**3. Relación entre el Sexo de las Víctimas y el Número de Víctimas :**

![Relación entre el Sexo de las Víctimas y el Número de Víctimas](https://github.com/Yuliedpardo/PI_DA/blob/main/imagenes/Sexo%20y%20nro%20V%C3%ADctimas.png)


1. Distribución por género:
   - El DataFrame presenta dos categorías principales de género: "FEMENINO" y "MASCULINO".
   - La categoría "FEMENINO" tiene 166 víctimas, mientras que "MASCULINO" tiene 545 víctimas.

2. Diferencia significativa en el número de víctimas:
   - Es evidente que hay una diferencia significativa en el número de víctimas entre los géneros. El género masculino tiene un número mucho mayor de víctimas que el género femenino.

3. Proporción de género:
   - Sería útil calcular la proporción de género para tener una comprensión más precisa de la relación entre las dos categorías. En este caso, la proporción de género masculino a femenino es aproximadamente 3.29:1.

4. Implicaciones y análisis adicional:
   - Esta diferencia en el número de víctimas entre géneros podría ser el resultado de múltiples factores, como la distribución de roles de género en la sociedad, la exposición a diferentes riesgos o la subnotificación de casos en función del género.

**4. Frecuencia por CATEGORIA EDAD:**

![Frecuencia por CATEGORIA EDAD](https://github.com/Yuliedpardo/PI_DA/blob/main/imagenes/Frecuencia%20por%20CATEGORIA%20EDAD.png)



1. Distribución por categoría de edad:
   - El DataFrame presenta tres categorías principales de edad: "Niños", "Adultos Jóvenes" y "Adultos Mayores".
   - La categoría "Niños" tiene 80 muertes por siniestros viales, la categoría "Adultos Jóvenes" tiene 262, y la categoría "Adultos Mayores" tiene 322.

2. Diferencias en el número de muertes por categoría de edad:
   - Existen diferencias significativas en el número de muertes por siniestros viales entre las categorías de edad. La categoría "Adultos Mayores" tiene el mayor número de muertes, seguida por "Adultos Jóvenes", mientras que "Niños" tiene el menor número de muertes.

3. Interpretación de los resultados:
   - Estas diferencias en el número de muertes por categoría de edad podrían estar relacionadas con la vulnerabilidad de cada grupo de edad en siniestros viales, así como con la exposición a diferentes riesgos en la carretera.

5. Análisis demográfico:
   - Sería útil considerar las características demográficas de cada grupo de edad, como la población total en cada categoría, para comprender mejor si estas diferencias son proporcionales a la población en riesgo.

6. Prevención y seguridad vial:
   - Estos datos pueden ser útiles para evaluar políticas y programas de seguridad vial dirigidos a grupos específicos de edad. Por ejemplo, si los "Adultos Mayores" tienen un alto número de muertes en siniestros viales, podría ser importante implementar medidas adicionales de seguridad para este grupo en particular, como campañas de concienciación y mejoras en las infraestructuras viales.

**5. Frecuencia de Tipos de Calle:**

![Frecuencia de Tipos de Calle](https://github.com/Yuliedpardo/PI_DA/blob/main/imagenes/Frecuencia%20de%20Tipos%20de%20Calle.png)


1. Distribución por tipo de calle:
   - El DataFrame presenta cuatro categorías principales de tipo de calle: "AUTOPISTA", "AVENIDA", "CALLE" y "GRAL PAZ".
   - La categoría "AVENIDA" tiene la mayor cantidad de víctimas por siniestros viales, con 442. Le sigue "CALLE" con 138, "GRAL PAZ" con 69 y "AUTOPISTA" con 68.

2. Diferencias en el número de víctimas por tipo de calle:
   - Existen diferencias significativas en el número de víctimas por siniestros viales entre los tipos de calle. "AVENIDA" tiene el mayor número de víctimas, mientras que "AUTOPISTA" tiene un número ligeramente menor.

3. Proporciones de víctimas por tipo de calle:
   - Calcular la proporción de víctimas en cada tipo de calle puede ayudar a comprender mejor la relación entre ellos. Por ejemplo, se podría calcular la proporción de víctimas en "AVENIDA" en relación con "AUTOPISTA" o la proporción de víctimas en "CALLE" en relación con "AVENIDA".

4. Interpretación de los resultados:
   - Estas diferencias en el número de víctimas por tipo de calle podrían estar relacionadas con la velocidad máxima permitida en cada tipo de carretera, el volumen de tráfico, la presencia de semáforos y señalización, y otros factores de seguridad vial.

5. Medidas de seguridad vial:
   - Los datos pueden ser útiles para evaluar la efectividad de las medidas de seguridad vial en diferentes tipos de carreteras. Por ejemplo, si "AVENIDA" tiene una alta cantidad de víctimas, podría ser necesario revisar las medidas de seguridad y la infraestructura en ese tipo de carretera.

**6. Distribución de Víctimas por Rol:**

![Distribución de Víctimas por Rol](https://github.com/Yuliedpardo/PI_DA/blob/main/imagenes/victimas_rol.png)

El DataFrame proporciona datos sobre el rol de las víctimas en siniestros viales, el tipo de vehículo involucrado y la cantidad de casos para cada combinación. 

1. Distribución de roles y tipos de vehículos:
   - El DataFrame muestra varias combinaciones de roles de víctimas y tipos de vehículos involucrados en siniestros viales.
   - Por ejemplo, hay conductores de autos, conductores de motos, ciclistas, pasajeros de autos, pasajeros de motos, peatones, y otros.

2. Número de casos:
   - El DataFrame también presenta el número de casos para cada combinación. Por ejemplo:

"CICLISTA" - "BICICLETA" - 29 casos:

Estos casos representan situaciones en las que la víctima era un ciclista que sufrió un siniestro vial mientras conducía una bicicleta.

"CONDUCTOR" - "AUTO" - 65 casos:

En estos casos, la víctima era el conductor de un automóvil. Las personas heridas estaban al mando de un vehículo destinado al transporte de personas.

"PEATON" - "PEATON" - 266 casos:

En estos casos, las víctimas eran peatones, es decir, personas que no se encontraban en ningún vehículo motorizado en el momento del siniestro. Estas personas sufrieron lesiones mientras caminaban.

"PASAJERO_ACOMPAÑANTE" - "AUTO" - 29 casos:


En estos casos, no se tiene información sobre el tipo de víctima, pero se sabe que estaban involucrados en siniestros viales con motocicletas.

"CONDUCTOR" - "MOTO" - 261 casos:

Estos casos representan situaciones en las que la víctima era el conductor de una motocicleta, ya sea una motocicleta estándar, un ciclomotor o un cuatriciclo.


En resumen, este DataFrame proporciona información detallada sobre la relación entre el rol de las víctimas y el tipo de vehículo involucrado en siniestros viales, junto con la cantidad de casos para cada combinación. Este análisis puede ser un punto de partida para abordar problemas de seguridad vial específicos y tomar medidas adecuadas para reducir los riesgos en las carreteras.

**7. Cantidad de Siniestros por Mes:**

![Cantidad de Siniestros por Mes](https://github.com/Yuliedpardo/PI_DA/blob/main/imagenes/victimas_por_mes.png)

El DataFrame proporciona datos sobre la cantidad de víctimas de siniestros viales en diferentes meses (representados por números del 1 al 12):

1. Distribución de víctimas por mes:
   - El DataFrame muestra el número de víctimas de siniestros viales para cada mes del año, desde enero (mes 1) hasta diciembre (mes 12).

2. Variación en el número de víctimas:
   - Hay variaciones en el número de víctimas de un mes a otro a lo largo del año. Por ejemplo, el mes 12 (diciembre) tiene el mayor número de víctimas con 81, mientras que el mes 8 (agosto) tiene 67 víctimas. El mes 7 (julio) tiene el menor número de víctimas con 51.

3. Estacionalidad:
   - Estos datos sugieren que podría haber una estacionalidad en los siniestros viales, con un aumento en el número de víctimas en los meses finales del año (noviembre y diciembre). Esto podría estar relacionado con factores como las condiciones climáticas, festividades o mayor actividad de tráfico en las vacaciones de fin de año.

4. Análisis de tendencias:
   - Para un análisis más detallado, se podrían utilizar técnicas de análisis de tendencias para identificar patrones estacionales y tendencias a lo largo del año. Esto podría ser útil para implementar medidas de seguridad vial específicas en momentos en que se observa un aumento en el número de víctimas.

5. Factores externos:
   - Es importante considerar factores externos que podrían influir en la cantidad de víctimas, como la aplicación de medidas de seguridad, el estado de las carreteras, la educación vial y el cumplimiento de las normas de tráfico.

6. Políticas de prevención:
   - Estos datos pueden ser útiles para evaluar la efectividad de las políticas de prevención de siniestros viales y para ajustar estrategias en función de las tendencias observadas en diferentes meses.


## KPIS



**KPI 1: Reducción del 10% en la tasa de homicidios en siniestros viales en CABA en comparación con el semestre anterior**

Este KPI se enfoca en medir la evolución de la tasa de homicidios en siniestros viales en la Ciudad Autónoma de Buenos Aires (CABA) en un período de varios años, comparando los dos últimos semestres.  Análisis más detallado:

- **Tendencia general:** La tendencia en este KPI varía año tras año. En algunos años, se logra una disminución significativa, mientras que en otros se observa un aumento en la tasa de homicidios en siniestros viales.

- **Año 2020:** Se destaca un aumento significativo en la tasa de homicidios en el primer semestre (61.29%), pero una mejora en el segundo semestre (10%), lo que puede ser atribuible a factores específicos, como el impacto de la pandemia o medidas de seguridad vial.

- **Año 2021:** Los datos parecen estar incompletos, ya que falta información para el segundo semestre. Esto puede dificultar una evaluación precisa del rendimiento en ese año.

- **Comparación entre semestres:** En algunos casos, se logra la reducción deseada del 10% entre semestres, mientras que en otros no se alcanza.

- **Análisis de causas:** Sería útil profundizar en las razones detrás de las variaciones en la tasa de homicidios en siniestros viales, como cambios en las políticas de seguridad vial, mejoras en la infraestructura vial, o la influencia de eventos externos como la pandemia.

![Reducción del 10% en la tasa de homicidios en siniestros viales en CABA en comparación con el semestre anterio](https://github.com/Yuliedpardo/PI_DA/blob/main/imagenes/victimas_por_mes.png)


**KPI 2: Reducción del 7% en la cantidad de accidentes mortales de motociclistas en CABA en el último año en comparación con el año anterior**

Este KPI se centra en evaluar la evolución de la cantidad de accidentes mortales de motociclistas en la Ciudad Autónoma de Buenos Aires (CABA) en un período de varios años, comparando los dos últimos años. Análisis más detallado:

- **Tendencia general:** En este KPI, también se observa una variación año tras año, con fluctuaciones tanto positivas como negativas.

- **Año 2020:** Destaca un aumento significativo del 64.29% en la cantidad de accidentes mortales de motociclistas, lo que podría requerir una atención inmediata para comprender las razones detrás de este aumento.

- **Año 2021:** Al igual que en el KPI 1, faltan datos para el año 2021 en este KPI, lo que dificulta una evaluación precisa.

- **Comparación anual:** La reducción del 7% en la cantidad de accidentes mortales de motociclistas es el objetivo, pero no siempre se logra. Por ejemplo, en el año 2019, se observa una disminución significativa del 44%.

- **Análisis de causas:** Para entender las fluctuaciones en este KPI, sería importante analizar factores como las medidas de seguridad específicas para motociclistas, el aumento en la cantidad de motociclistas en la ciudad y la aplicación de políticas de tráfico.

![Reducción del 7% en la cantidad de accidentes mortales de motociclistas en CABA en el último año en comparación con el año anterio](https://github.com/Yuliedpardo/PI_DA/blob/main/imagenes/victimas_por_mes.png)



**KPI 3: Análisis del Índice de Víctimas por Siniestros Viales por Comuna (por cada 100,000 habitantes):**

1. **Objetivo**:
   - Este KPI evalúa la tasa de víctimas por siniestros viales por cada 100,000 habitantes en cada comuna, lo que proporciona información importante sobre la seguridad vial en diferentes áreas.

2. **Datos de Entrada**:
   - Los datos incluyen 15 comunas etiquetadas del 0 al 14.
   - Cada comuna tiene dos variables: el número de víctimas por siniestros viales (N_VICTIMAS) y el índice de víctimas por siniestros viales (INDICE_VICTIMAS).

3. **Interpretación del Índice de Víctimas por Siniestros Viales**:
   - El índice de víctimas por siniestros viales es un valor decimal que representa la cantidad de víctimas por cada 100,000 habitantes en la comuna.
   - Un índice más alto indica una tasa de siniestros viales más alta en relación con la población.

4. **Resumen de los Datos**:
   - La comuna 8 tiene la mayor cantidad de víctimas por siniestros viales (16) por cada 100,000 habitantes y el índice de víctimas más alto (0.652538), lo que sugiere una tasa de siniestros viales significativamente alta en relación con su población.
   - La comuna 5 tiene la menor cantidad de víctimas por siniestros viales (1) por cada 100,000 habitantes y el índice de víctimas más bajo (0.032627), lo que indica una tasa de siniestros viales baja en relación con su población.
   - Las comunas 0, 2, 3, 4, 6, 9, 10, 11, 12, 13 y 14 también tienen índices de víctimas por siniestros viales superiores a 0.1 por cada 100,000 habitantes, lo que indica niveles moderados de siniestros viales en relación con sus poblaciones.
   - Las comunas 1 y 7 tienen índices de víctimas por siniestros viales entre 0.1 y 0.5 por cada 100,000 habitantes, lo que sugiere niveles intermedios de siniestros viales en relación con sus poblaciones.

5. **Tendencias y Patrones**:
   - Se pueden identificar tendencias y patrones similares a los mencionados anteriormente, pero ahora se considera la tasa de siniestros viales por cada 100,000 habitantes, lo que proporciona una perspectiva más precisa en relación con la población.

6. **Acciones Recomendadas**:
   - Para las comunas con índices de víctimas por siniestros viales altos por cada 100,000 habitantes, se deben implementar medidas adicionales de seguridad vial, como mejoras en señalización, control de velocidad y educación vial, teniendo en cuenta la densidad poblacional.
   - Para las comunas con índices de víctimas por siniestros viales bajos por cada 100,000 habitantes, es importante mantener un monitoreo constante y continuar aplicando políticas de seguridad vial para mantener los niveles bajos de siniestros en relación con la población.

Este análisis corregido toma en cuenta que el índice de víctimas se refiere a la cantidad de víctimas por cada 100,000 habitantes, lo que proporciona una evaluación más precisa de la seguridad vial en cada comuna en relación con su población.

![Análisis del Índice de Víctimas por Siniestros Viales por Comuna (por cada 100,000 habitantes](https://github.com/Yuliedpardo/PI_DA/blob/main/imagenes/victimas_por_mes.png)



Estos KPIS se alimentan con datos del archivo CSV resultante del análisis exploratorio de datos (EDA) realizado anteriormente. 

*Todo este proceso de desarrollo se llevó a cabo de manera local en **Visual Studio Code (VSCODE)**, haciendo uso de **Jupyter Notebook**, **Python, numpy, pandas, FastAPI y uvicorn**. Esta amalgama de herramientas tecnológicas permitió dar vida a los puntos finales de la API, desplegando de manera exitosa el acceso a las funciones y capacidades desarrolladas en el proyecto.*



Este proceso integral, que abarcó desde la transformación de datos hasta el análisis exploratorio y la construcción de soluciones tecnológicas avanzadas, encapsula la esencia misma del proyecto. Cada paso contribuyó de manera sinérgica para dar vida a una plataforma sólida y versátil, preparada para ofrecer recomendaciones precisas y una experiencia de usuario excepcional.

*Todo este proceso fue desarrollado localmente en **Visual Studio Code (VSCODE)** utilizando **Jupyter Notebook** como nuestro entorno de trabajo principal. La combinación de herramientas tecnológicas que empleamos incluye **Python** como lenguaje de programación, junto con bibliotecas esenciales como **numpy y pandas** para la manipulación eficiente de datos. Además, utilizamos **matplotlib y seaborn** para la creación de visualizaciones gráficas impactantes, que nos permitieron revelar patrones y tendencias ocultas en los datos de manera efectiva.*
