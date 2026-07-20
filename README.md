# Relación entre productividad económica y movilidad urbana  /  Relationship between economic productivity and urban mobility  

## ES Español (English below)

**Rol:** Analista de Datos (Prácticas).
**Herramientas:** Jupyter Notebook, Python (Pandas, Numpy, Scipy, Matplotlib, Seaborn).
**Habilidades:** Exploración y limpieza de base de datos, diseño y planificación de visualizaciones.

### Descripción del proyecto
Proyecto de Bootcamp TripleTen para crear en Jupyter Notebook un reporte para el American Development Bank con el fin de entender cómo la movilidad urbana (niveles de congestión, tiempos de viaje, retrasos) se relaciona con la productividad económica (PIB per cápita, desempleo) en las principales ciudades del mundo.

### Objetivos del proyecto
El objetivo primordial del banco es identificar en qué ciudades invertir en infraestructura de transporte para aumentar la productividad y el bienestar de la población. Las preguntas concretas a responder son:
- ¿Qué ciudades presentan alta congestión y baja productividad económica?
- ¿Cuáles muestran los mejores indicadores combinados (movilidad eficiente y economía fuerte)?
- ¿Qué variables parecen tener una relación más fuerte con el desarrollo urbano?

### Preparación de los datos  
Para este estudio, se usaron dos datasets principales, los cuales se unieron para crear el dataset para el análisis final:
- tomtom_traffic.csv: datos sobre congestión vehicular y condiciones de tráfico en ciudades del mundo.
- oecd_city_economy.csv: indicadores económicos y ambientales por ciudad, recopilados por la OECD (Organización para la Cooperación y el Desarrollo Económico).
- ladb_mobility_economy_2024_clean.csv: unión de ambos datasets tras realizar la limpieza y normalización de datos y poder entender cómo la eficiencia del tráfico urbano se relaciona con el desempeño económico.

#### Tareas realizadas:  
- Carga y exploración de datos (identificación de columnas, tipos de datos y estructura general de ambos datasets).
- Limpieza y correción: estandarización de nombres de columnas y correción de tipos de datos.
- Extracción y filtrado: se trabajó solamente con el periodo más reciente (2024), extrayendo el año y filtrando resultados.
- Cálculo de promedios de tráfico por ciudad para obtener una vista consolidada de la movilidad urbana.
- Unión de los dos datasts tomando como llave de unión la ciudad.
- Boxplot para visualizar la distribución del tráfico (media, mediana y valores atípicos).
- Histograma para analizar la forma de la distribución y el valor promedio del PIB per cápita. 
- Informe ejecutivo con implicaciones y reflexiones sobre la relación entre economía y movilidad.

### Hallazgos clave
El análisis nos muestra que en aquellas ciudades donde la congestión y los tiempos de traslados son menores, el PIB per cápita es mucho mayor. Solamente hay tres ciudades que rompen con este patrón: Ciudad de México, Sao Paulo y Bogotá, sin embargo, este comportamiento puede deberse a que son ciudades densamente pobladas y los tiempos de viaje y congestión vehicular se ven siempre afectados por la insuficiente infraestructura.
El estudio fue revisando las columnas con datos de cada Dataset y se fueron eliminando los datos que no fueran relevantes. Se consideraron aquellos datos importantes para responder a las preguntas, tales como los tiempos de viaje, métricas de tiempo y sobre todo, las del PIB, todas agrupadas con datos geográficas (es decir, ciudades y países), limitando todo esto al año 2024.
En general, las ciudades con mayor PIB tienen poca congestión, a excepción de la Ciudad de México, Sao Paulo y Bogotá, donde la congestión está por encima del PIB promedio. Esto puede deberse también a que son ciudades densamente pobladas. Pero también habría que revisar el impacto que tiene el hecho de que los tres valores máximos en la columna de jams_delay aparecen justamente para estas ciudades, y particularmente en Ciudad de México y Sao Paulo son sospechosamente altos (marcando el valor máximo y el outlier en el BoxPlot "Jams_Delay"). Fuera de esas tres ciudades, encuentro que un PIB alto tiene una relación directa con niveles de congestión mucho más bajos.
En la columna de Jams_Delay, el BoxPlot nos muestra que la gran mayoría de los valores están por debajo de los 900 minutos; sin embargo, se buscaron aquellas filas que estuvieran por encima de este valor y el resultado fueron cuatro ciudades: Lima, Bogotá, Sao Paulo y Ciudad de México. Las primeras dos realmente no se distancian mucho del espacio en donde se encuentran la mayoría de los datos, sin embargo, Sao Paulo, con un valor de 1,729 minutos (representado en el BoxPlot como "máximo") y Ciudad de México, con valor de 2,833 (representado como "outlier" en el BoxPlot) nos reflejan valores sospechosamente altos que habría que revisar a detalle, ya que esos valores tan altos podrían estar creando distorsión en la gráfica de columnas donde comparamos PIB vs Congestión.

### Recomendaciones
Sin duda el primer paso es revisar los valores de Ciudad de México, Sao Paulo y Bogotá para explorar de dónde vienen esos outliers que parecen inflar los valores de jams_delay y por ende rompen con el patrón hallado en el gráfico de columnas donde vemos una relación directa entre Alto_PIB / Baja_Congestión. En caso de que las lecturas sean correctas, habría entonces que pensar en medidas urgentes para mejorar la movilidad y disminuir el tráfico en esas ciudades que salen tan marcadamente del patrón que las otras ciudades latinoamericanas tienen.
Las dos ciudades que requieren mayor atención son Ciudad de México y Sao Paulo. Si sus mediciones son correctas, estas dos ciudades tienen un valor más alto de congestión vs. el PIB, reflejando una importante necesidad de mejorar el tema de movilidad urbana.

---

# Relationship between economic productivity and urban mobility 

## EN English (Spanish above)

**Role:** Data Analyst (Intern).
**Tools:** Jupyter Notebook, Python (Pandas, Numpy, Scipy, Matplotlib, Seaborn).
**Skills:** Database exploration and data cleaning, visualization design and planification.

### Project description
TripleTen Bootcamp project for the creation on Jupyter Notebook of a report for the American Development Bank to understand how urban mobility (traffic jams, travel times and delays) relate to economic productivity (PIB per cápita, unemployment) in the main cities of the world. 

### Project goals
The bank´s main goal is to identify in which cities they have to invest in transport infrastructure in order to raise the productivity and life quality of the population. Concrete questions are:
- Which cities have the higher traffic jams and the lowest economic productivity?
- Which cities show the best combined indicators (eficient mobility and healthy economy)?
- Which variables seem to have a stronger relationship with urban development? 

### Data preparation  
Two main datasets were used for this analysis, joinning them into a third one used for the final report:  
- tomtom_traffic.csv: dataset with information about jams delays and traffic conditions in several cities of the world.
- oecd_city_economy.csv: economic and environmental indicators by city, gathered by the OECD (Organization for Cooperation and Economic Develepment).
- ladb_mobility_economy_2024_clean.csv: join of both datasets after cleaning and normalization of data, in order to understand traffic eficiency related to economic development. 

#### Tasks performed:  
- Data load and exploration (identifying columns, data types and the general structure of both datasets).
- Cleaning and validation: column name standarization and validation of data tyoes.
- Extracción and filtering: the analysis was based on the most recent period (2024) so this year was extracted and filtered.
- Average estimations for traffic per city to get an overview of urban mobility.
- Join of both datasets using city as the key.
- Boxplot to visualize traffic distribution (mean, median and outliers).
- Histogram to analyze the distribution and average value of PIB per capita.
- Executive report with implications and comments on the relationship between economy and mobility.

### Key Findings
Following the SCQA model, we have these findings:

- S (Situation): in the Overview, the line graphic shows that both in 2024 and 2025 (as well as joining the two years), there´s a clear decrease during the winter months.
- C (Complication): after reviewing the bar graphs, we realize that the "economic" customer´s profile as well as Colombia show values under the general average.
- Q (Question): What´s going on during the winter and how are other variables moving depending on the country?
- A (Answer): the sales fall abruptly during the winter and Colombia has very low sales at all the product categories.

- S (Situation): the three regions of Colombia have both a Total Revenue and Amount of Sales below the general average.
- C (Complication): the low values from Colombia match the low amount of requests in that country (compared to the average and the other country. We also notice that the "economic" customer profile is very low all the countries.
- Q (Question): What is causing the low sales in Colombia and the weakness of the "Economic" customer´s profile?
- A (Answer): the seasonality influences, since we notice that profit and total sales decrease in all the countries, but further measures and analyses have to be performed particularly for Colombia in all the product categories and with the "economic" customer´s profile in general.

### Recommendations
Sales fall abruptly during winter (both profit and amount of properties sold). More concerning is Colombia, where sales are very low for all the property categories. Also, it´s important to analyze the weakness of the "economic" customer´s profile. Marketing has to focus on these red spots.
Customer´s retention is very low, which is expected in this business, where only the "investor" customer´s profile stays active for longer periods.
