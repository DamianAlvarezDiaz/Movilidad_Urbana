# Movilidad Urbana: análisis exploratorios y visualizaciones en Python

## ES Español (English below)

**Rol:** Analista de Datos (Prácticas).
**Herramientas:** Jupyter Notebook, Python (Pandas, Numpy, Scipy, Matplotlib, Seaborn).
**Habilidades:** Exploración y limpieza de base de datos, diseño y planificación de visualización.

### Descripción del proyecto
Proyecto de Bootcamp TripleTen para crear en Power BI un dashboard de análisis comercial inmobiliario, para comprender mejor el desempeño comercial de diferentes tipos de propiedades a través de distintos canales de venta y segmentos de clientes.

### Objetivos del proyecto
El dashboard ayuda a responder preguntas como:
- ¿Cuál es el ingreso total generado por las ventas de propiedades?
- ¿Qué tipo de propiedad genera más ingresos?
- ¿Qué segmentos de clientes compran más?
- ¿Cómo evolucionan las ventas en el tiempo?
- ¿El negocio está creciendo año contra año?
- ¿Los clientes vuelven a comprar después de su primera compra?

### Preparación de los datos  
Se limpiaron e integraron tres datasets principales, adjuntas en este repositorio:  
- dim_clientes.csv: contiene los datos de los clientes.
- dim_propiedades.csv: información completa de las propiedades.
- hecho_ventas_propiedades.csv: datos transaccionales de las ventas.

#### Tareas realizadas:  
- Conversión de tipos y normalización de fechas.
- Creación en Power BI de una nueva tabla para manejar datos temporales (dim_fechas).
- Cálculo de estadísticas básicas para medir el desempeño comercial.  
- Unión de datasets por claves comunes para análisis completo.
- Diseño y creación de gráficos para visualizar y responder a los objetivos del proyecto.

### Desempeño general
- KPIs clave para visualizar el panorama general: ingreso total, cantidad de ventas, ticket promedio, comisión total y Crecimiento YoY (Year-Over-Year).
- Gráfico de líneas: Ingreso total por mes a lo largo del tiempo.
- Gráficos de barras: uno con Cantidad de ventas por ciudad y otro con Ingreso total por ciudad.
- Segmentadores: temporal (por año) y por tipo de cliente. Estos segmentadores ayudan a ver rápidamente las estadísticas generales y gráficos anteriores según los filtros de los segmentadores.

### Análisis Comercial
Gráficos de barras que profundizan en diversos aspectos del desempeño de la empresa:
- Ingreso total y cantidad de ventas por tipo de propiedad.
- Ingreso total y cantidad de ventas por canal de venta.
- Ingreso total y cantidad de ventas por segmento de cliente.
Se agrega también una tabla con el ingreso total, la cantidad de ventas y el ticket promedio

### Análisis de retención de cohortes
Matriz con la retención de cohortes. Puede ser segmentada por el tipo de cliente y por ciudad.

### Hallazgos clave
Siguiendo el modelo SCQA, tenemos los siguientes hallazgos:

- S (Situación): en el Overview, el gráfico de líneas nos muestra que tanto en 2024 como en 2025 (y al unir los dos años también), hay una notoria caída en los meses de invierno.
- C (Complicación): al ver los demás gráficos de barras, nos damos cuenta de que el segmento de cliente "Económico" y Colombia muestran valores por debajo del promedio.
- Q (Pregunta: ¿Qué está pasando en el Invierno y cómo se distribuyen diferentes variables por país?
- A (Respuesta): las ventas caen abruptamente en invierno y Colombia tiene niveles muy bajos en todas las categorías de productos.

- S (Situación): las tres regiones de Colombia tienen una utilidad total y una cantidad de unidades vendidas por debajo del promedio.
- C (Complicación): los valores bajos de Colombia corresponden con mantener cantidades de pedidos muy por debajo de los otros dos países y del promedio. También vemos que el segmento "Económico" es muy bajo en los tres países.
- Q (Pregunta): ¿Qué está causando las ventas bajas en Colombia y la debilidad en el segmento "Económico"?
- A (Respuesta): la estacionalidad influye, ya que notamos una caída en la utilidad y las unidades vendidas en todos los países, pero se deben tomar medidas y revisiones más detalladas respecto a lo que está pasando en Colombia en todas los categorías de productos y en particular con el segmentos "Económico" para todos los países.

### Recomendaciones
Las ventas caen abrupamente en Invierno (tanto la utilidad como la cantidad de propiedades vendidas). Más preocupante es el mercado de Colombia, que tiene ventas muy bajas en todos los productos y se debe profundizar también en la debilidad de los clientes del segmento "económicos". Atención a marketing sobre estos focos rojos.
La retención de clientes es muy baja, lo cual es de esperarse en este tipo de negocio, donde solamente el tipo de cliente "inversionista" se mantiene activo por más tiempo.

---

# Commercial Performance Dashboard for the Real Estate Andes Capital company

## EN English (Spanish above)

**Role:** Data Analyst (Intern).
**Tools:** Power BI, Jupyter Notebook.
**Skills:** Database exploration and data cleaning, visualization design and planification, dashboard storytelling using the SCQA model (Situation, Complication, Question, Answer), cohort analysis.

### Project description
TripleTen Bootcamp project for the creation of a Power BI dashboard for commercial analysis in a Real Estate company, in order to understand the commercial performance of different classes of properties throughout sales channels and customer profiles.

### Project goals
The dashboard will help to answer questions like:
- What is the total revenue from property sales? 
- What kind of property generates the major income?
- Which customer profile purchases more?
- How does the sales evolve across time?
- Is the business growing year over year? 
- Do the customers buy again after their first purchase? 

### Data preparation  
Three different datasets were cleaned and integrated (attached in the repository files):  
- dim_clientes.csv: contains all the data from the customers.
- dim_propiedades.csv: complete information regarding the properties.
- hecho_ventas_propiedades.csv: transactional data of the properties´ sales.

#### Tasks performed:  
- Data type conversion and date noramlization.
- Creation of a new table in Power BI, to manage tempral data (dim_fechas).
- Basic statistics to mesure the commercial performance.  
- Datasets union using primary keys for a full analysis.
- Graphic design and creation in order to visualize and answer the project goals.

### General Performance
- Key KPIs to visualize the general overview: Total revenue, Amount of sales, Average ticket, Total comission and YoY Growth.
- Line graph: Total revenue per month across time.
- Bar graph: one for Amount of Sales per City and another one for Total Revenue per City.
- Slicers: temporal (per year) and by customer´s profile. These slicers help to quickly visualize the basic stats and graphs above-mentiones based on the slicer´s filters.

### Commercial Analysis
Bar graphs that deeply analyze several aspects of the company´s performance:
- Total revenue and Amount of Sales by Property Type.
- Total revenue and Amount of Sales by Sales Channel.
- Total revenue and Amount of Sales by Customer´s Profile.
A table with total revenue, amount of sales and average ticket is also included.

### Cohort Retention Analysis
Matrix with the cohort retention. It can be filtered by customer´s profile and by city.

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
