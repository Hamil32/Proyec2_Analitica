<p align=center><img src=https://assets.soyhenry.com/logos/LOGO-HENRY-04.png><p> 
# PROYECTO INDIVIDUAL N°2 - Analítica de DATOS

## *Desarrollado por Hamil Flores Balverdi para Henry´s bootcamp* 


#### Problemática:
- **Simulación** una empresa busca invertir sus ganancias para poder maximizar sus beneficios, para ellos se pone en contacto con nosotros Company. S.A. donde se pide al deparamento de Data Analytics que hiciera reomendaciones de inversion, utilizando un grupo de [datasets(https://github.com/Hamil32/Proyec2_Analitica/tree/main/labs2/data5empresas) provistos, realice las **transformaciones requeridas** y posteriormente **ponga a disposición los datos** mediante la elaboración y ejecución de un **Dashboard** con diferentes **KPIS**.

#### Rol del desarrollador:
- Data Analitics

<hr> 

### Proceso de "ETL" (Extract, transform, load) en VisualStudioCode - Python:

`EXTRACCIÓN DE DATOS`


1. Importación de la librería yfinance, pandas para el manejo de dataframes
2. Ingesta de datos (Archivos .csv) en respectivos dataframes (S&P500, Amazon, Apple, Meta, Microsoft, Tesla)
3. Análisis exploratorio de los distintos datasets para conocer sus características principales
   
`TRANSFORMACIONES`

1. Reemplazo de code por Fecha
2. Generación del campo ID con Fecha
3. Unificar 5 plataformas a través de la función “concat” en un dataframe único "dfCompleto" facilitando el código de las consultas a desarrollar
4. Exportar CSV final ("completo.csv") con todas las transformaciones
##### *Nota: La extracción de datos así como las respectivas transformaciones pueden verse desarrolladas en el archivo [codigo.ipynb]( https://github.com/amysler/Proyecto_individual_data_engineer-Henry_bootcamp-DTS06/blob/main/ETL.ipynb)*
  
  <hr> 

### Breve introduccion de la Teoria Dow

La teoría de Dow es un enfoque de análisis técnico para predecir las tendencias del mercado. Fue desarrollado por Charles Dow a finales del siglo XIX y se basa en la idea de que los precios de los activos reflejan todas las noticias y eventos relevantes. La teoría sostiene que los mercados se mueven en tendencias alcistas, bajistas o laterales, y que estas tendencias se pueden identificar a través de la observación de los movimientos de los precios y los volúmenes de negociación. Además, la teoría de Dow establece que las tendencias suelen tener tres fases: una fase de acumulación, una fase de impulso y una fase de distribución.

### Desarrollo del analisis tecnico S&P500:

<p align=center><img src=https://github.com/Hamil32/Proyec2_Analitica/blob/main/labs2/S%26P500GRAFICO.png><p>

En este grafico vamos a prestar  atencion en el rango de fecha 2009-02-02 hasta el 2021-12-01
Podemos ver claramente una tendencia alcista con un angulo en la tendencia de 46° algo q es muy saludable.
Luego vamos a prestar atencion en una fraccion de ese periodo en fecha 2020-03, donde se ve muy pronunciada esa tendencia, si verificamos su angulo nos muestra que es de 79° algo que es muy dificil de sostener, lo cual produce un retroceso del 50% para el 2022-09 algo muy normal para una subida tan brusca.
Y a continuacio se pede notar que se esta produciondo un patron ABC lo que me alerta a un posible hecho lateral o de consolidacion en el precio que estaria rondando en rango de los $3632 a $4200.
Otro indicador muy importante usado en este analisis es la EMA (Exponential Moving Average) ya que se puede observar que cuando el precio a alcanzado a tocar esa linea (color=azul)su comportado fue a traves de impulsos y en busca de nuevos maximos.
Observacion: a traves de este analisis podemos considerar que entrar en LONG a precios de $3700 podria ofrecer beneficios de 28% por cada dolar invertivo si buscamos salirnos en zona de maximo cercanos a los $4750. En cuanto al tiempo podriamos hacer una aproximacion a la fecha de en el año 2025. Lo que indicaria una rentablidad anual al 14%

<hr>

 ###Creacion de Dashboard S&P500
1. Se realizo un grafico de linea utilizando diferentes temporalidades (5dias, 1mes, 6meses, YTD, 5 Años, Max).
2. Se creo una tabla con los valores de cotizacion con su fecha especifica.
3. Generación de kpis con media moviles de 50 y 20 periodos.
4. Declaracion de etiqueta en valor de cotizacion promedio y su valor Max.

<hr>
### Utilizacion de KPIS
Media movil 20 y 50: 
1:Establecer un objetivo: visualizar si esta media movil se encuentra por encima o por debajo del precio de cotizacion.
Establecer un indicador numérico: promedio de los ultimos 20 y 50 periodos
Establecer un plazo: en el año 2023 el precio ha bajado notablemente y la media movil nos da una buena opcion para la entrada en posicion.
Establecer una meta: cuando se cruzan estas media moviles nos dara el punto de mejor entrada para tomar posicion.
Monitorear y medir: Finalmente, es importante monitorear y medir regularmente el progreso hacia el objetivo establecido.

<hr>

 ###Creacion de Dashboard Amazon, Apple, Meta, Microsoft, Tesla (Desde 2019 - 2023)
 1. Creacion de grafico de lineas con el precio de cotizacion y la media movil de 20 periodos para cada grafico.
 2. Declaracion de etiqueta del precio Minimo que tuvo la cotizacion, segun fecha seleccionada.
 3. Declaracion de etiqueta del precio maximo que tuvo la cotizacion, segun fecha seleccionada.

<hr>
###Recomendacion de inversion

Despues de comparar los datos de las 5 empresas mas representativas del indice S&P 500 (Apple= AAPL, Microsoft=MSFT, Amazon=AMZN, Tesla=TSLA, Facebook=META)
Estamos listo para hacer una recomendacion para nuestra empresa que busca incrementar sus beneficios exponencialmente a bajo riego.
Para ello recomendamos una estrategia de indexacion con un toque mas activo en las empresas anteriormente mencionadas.
La compocion de la cartera seria 50% = SPY, 10% = AAPL, 10% MSFT, 10% = AMNZ, 10% = TSLA, 10% = META.
Esta estrategia busca generar rendimientos del 20% anual.
Esto lo hemos determinado asi ya que estas 5 empresas componen el 75% del valor del indice S&P500. (Utilizamos el cruce de la media movil 20 sobre los precios de cotizacion para determinar si se esta comprando barato o no)
<hr>

### Proceso de puesta a disposición los datos: 
1. Generación de archivo [main.py](https://github.com/Hamil32/Proyec2_Analitica/blob/main/README.md)
2. Importación de las librerías a utilizar
4. Declaración de la ruta de acceso para la base de datos (completo.csv)


#### Tecnologías utilizadas:
- Visual studio code
- Python
- Power bi
- yfinance librery
- Pandas library
- github
