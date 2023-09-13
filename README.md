<!-- TABLA DE CONTENIDO -->
<details>
  <summary>Tabla de contenido</summary>
  <ol>  
    <li><a href="#Introducción">Introducción</a></li>
    <li><a href="#Objetivo">Objetivo</a></li>
    <li><a href="#ámbito-de-proyecto">Ámbito de Proyecto</a></li>
    <li><a href="#ETL_EDA">ETL_EDA</a></li>
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

A medida que se desentrañaban los entresijos de los datos, se tomaron decisiones críticas que influyeron en la dirección del proyecto. La identificación de patrones y atributos relevantes se convirtió en un pilar esencial para construir la base de las funciones API y el sistema de recomendación que se desarrollaría posteriormente. La calidad del análisis realizado durante el EDA estableció el terreno para la creación de soluciones sólidas y eficientes que aprovecharían al máximo la información extraída de los datos procesados en la etapa de ETL.



![victimas por comunas]([imagen.png](https://github.com/Yuliedpardo/PI_DA/blob/main/imagen.png))

Este proceso integral, que abarcó desde la transformación de datos hasta el análisis exploratorio y la construcción de soluciones tecnológicas avanzadas, encapsula la esencia misma del proyecto. Cada paso contribuyó de manera sinérgica para dar vida a una plataforma sólida y versátil, preparada para ofrecer recomendaciones precisas y una experiencia de usuario excepcional.

*Todo este proceso fue desarrollado localmente en **Visual Studio Code (VSCODE)** utilizando **Jupyter Notebook** como nuestro entorno de trabajo principal. La combinación de herramientas tecnológicas que empleamos incluye **Python** como lenguaje de programación, junto con bibliotecas esenciales como **numpy y pandas** para la manipulación eficiente de datos. Además, utilizamos **matplotlib y seaborn** para la creación de visualizaciones gráficas impactantes, que nos permitieron revelar patrones y tendencias ocultas en los datos de manera efectiva.*
