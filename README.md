![henry](https://github.com/flormiranda1/Cryptocurrency-Data-Analytics/blob/main/imagenes/henry.jpg)

# Cryptocurrency-Data-Analytics

<div align="center">
  <img src="https://github.com/flormiranda1/Cryptocurrency-Data-Analytics/blob/main/imagenes/crypto.png" alt="cryptoimage" width="200" height="200" />
</div>

¡Bienvenidos a mi último proyecto individual de la etapa de labs en el bootcamp de Henry! En esta oportunidad les presentaré un proyecto de principio a fin de data analytics sobre el mercado de las cryptomonedas, tomando como base para el análisis 10 cryptomonedas que fueron las que mayores ganancias generaron el último año debido a su cambio de precio.

## **Descripción del problema**

En la actualidad, el mercado de las criptomonedas ha experimentado un crecimiento vertiginoso, presentando oportunidades de inversión y ganancias considerables para aquellos que han tomado decisiones financieras informadas. Sin embargo, este mercado también es altamente volátil y está sujeto a cambios impredecibles. Ante este panorama, se plantea la necesidad de analizar detenidamente el rendimiento de las 10 criptomonedas más rentables durante el último año, con el fin de brindar información valiosa al inversor de mediano plazo

En este proyecto de análisis de datos, se abordará el desafío de seleccionar y examinar las 10 criptomonedas que han generado las mayores ganancias en el transcurso del último año. Para ello, se recopilarán datos históricos de precios, volúmenes y capitalización de mercado de estas criptomonedas. Se aplicarán técnicas de análisis y visualización de datos. La información extraída permitirá identificar patrones de comportamiento, tendencias alcistas y bajistas, así como factores clave que han influido en su rendimiento y que pueden tomarse en cuenta a la hora de hacer una inversión

## **Objetivos del Proyecto**

- Identificar las 10 criptomonedas que han generado las mayores ganancias en el último año.
- Analizar las tendencias de precios y volúmenes de estas criptomonedas a lo largo del tiempo.
- Explorar correlaciones existentes entre ellas
- Proporcionar insights y recomendaciones basadas en el análisis inversores a corto/mediano plazo.

## **Flujo de trabajo**

El flujo de trabajo se comienza con una primera eta de "Análisis exploratorio de los datos" (EDA) para identificar valores faltantes, atípicos, registros duplicados y patrones en los datos.
Luego a partir de las conclusiones sacadas en el EDA, se pasa a la instancia del diseño y armado de dashboard en base a los objetivos planteados.
Por último se sacan las conclusiones de los resultados del dashboard y se presentan KPIs que servirán como insights para un inversor a mediano/corto plazo.

### EDA
En el archivo de jupyter notebook llamado "EDA" que se encuentra en el repositorio podemos ver el proceso que se llevo a cabo en esta etapa, con sus respectivas conclusiones.
Como resultado de este EDA tenemos unos archivos csv que se guadaron en la carpeta data_csv para poder trabajar en base a ellos en nuestro dashboard:
- market: data actual de cada moneda
- all_coins: data histórica del compartamiento de precios, market_cap y volumen de las 10 monedas juntas
- coin_id.csv: data de cada moneda en particular, tiene la misma información que all coins pero separada en un data frame por moneda. Lo separé en caso que el archivo all_coins me generara algún inconveniente en el dashboard

### Dashboard
Se diagramó el dashboard primeramente según los objetivos y luego se pasó a su construcción con la herramienta de PowerBI, en él encontraremos una portada con botones interactivos a las diferentes páginas, un análisis general de tendencias históricas de precios, volúmenes y capitalización de mercado, también interactivo para ver el comportamiento de cada moneda en particular y por fechas específicas.
Por otro lado encontrarán en las hojas subsiguientes los KPIs que le servirán al inversor para la toma de decisiones

### Informe de análisis: conclusiones
- La mayoría de las monedas (bitcoin, rollbit-coin,okb, ripple, xdce, litecoin, bitget-token, kaspa) tienen un comportamiento de market_cap lineal con respecto al precio, es decir que a medida que el precio aumenta, el market_cap también lo hace en igual medida

- En cuanto al volumen de transacciones, se observa un comportamiento mayoritariamente estable, con picos lógicos en momentos de picos de precio

- Entre los años 2018 a 2021 se observa una tendencia general estable, luego se ve un alza en los precios desde el año 2019 hasta 2022, con sus mayores picos en el mes de noviembre de dicho año. En el corriente año se nota una tendencia al alza en los precios pero no de manera tan abrupta
  
- Se puede observar que la mayoría de las monedas (6) perteneces al **Ecosistema de Ethereum**, es ecosistema es una plataforma descentralizada con su propia blockchain y un ecosistema completo donde todos pueden construir varias aplicaciones distribuidas (Dapp), contratos inteligentes e incluso sus propias criptomonedas. Todas ellas tienen como objetivo ser seguras de usar y fiables, y no hay necesidad de intermediarios como bancos o agencias. Todo es accesible y legible para todos, así que es fácil evitar ser estafado, por lo cual se recomienda mayormente la inversión en monedas que pertenecen a este ecosistema

- Podemos observar como el precio de algunas monedas siguen la tendencia de los precios de otras:
  injective-litecoin-bitcoin
  injective-ripple-kaspa-bitgettoken-okb
  ripple-bitcoin-litecoin

- Se puede ver, y tiene sentido, que estas 10 cryptomonedas que generaron mayores ganancias el pasado año, están en el top 100 del raniking de market_cap, siendo 2 del top_10 y 3 del top_50

### KPI´s

En esta sección se presentarán 3 KPI´s que servirán como insights para la toma de decisión del inversor a corto/mediano plazo:

- Precio actual: Se proporciona el dato del precio actual y se toma como referencia la media móvil a 30 días, si este precio actual está por debajo de la media móvil, se considera una oportunidad buena de inversión
- Porcentaje de cambio en 24hs: Si este porcentaje es positivo, significa que el precio viene al alza por lo que no se recomienda hacer inversión, si el porcentaje es negativo, y el precio actual se encuentra por debajo de la media móvil estamos ante una buena oportunidad
- Riesgo de inversión: Se establece un riesgo máximo aceptable (lo que se está dispuesto a perder de la inversión inicial) y se calcula el porcentaje de cambio acumulado en los últimos 30 días, si la variación acumulada en los últimos 30 días es mayor a nuestro riesgo máximo aceptable entonces se trata de un riesgo elevado, por lo que no es recomendable invertir.
