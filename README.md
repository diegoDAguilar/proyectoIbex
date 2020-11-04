# Análisis exploratorio del IBEX 35

1. Hipótesis.
2. Metodología.
3. Obtención de los datos.
4. Preparación de los datos.
5. Búsqueda del comparador.
6. Conclusiones

## Hipótesis
Las empresas están relacionadas con otras de su mismo sector, por tanto debería ser posible extraer dichos sectores estudiando las relaciones de correlación entre cada empresa.

## Metodología
Serán necesarios los datos del valor de las acciones de las 35 empresas más relevantes de las Bolsas españolas. Después de comprobar que los datos estén completos se procederá a buscar relaciones de correlación entre cada empresa y las demás. Para ello habrá que encontrar primero el valor que represente mejor el crecimiento de cada empresa. A partir de las corelaciones se crearán grupos entre empresas próximas entre sí, esperando que coincidan con sectores distintos del mercado.

## Obtención de los datos
Se descargan 35 datasets de la web Investing.com correspondientes a cada una de las empresas que figuran en el IBEX 35 en octubre de 2020. Estos datasets contienen la información sobre el precio de sus acciones para cada día entre enero de 2015 y diciembre de 2019. Es decir, 5 años.

## Preparación de los datos
Para poder llevar a cabo las correlaciones con éxito es importante que la información de los datasets corresponda a las mismas fechas, por tanto se crea un dataframe con los nombres de las empresas en sus columnas y las fechas en los valores. Así se obtiene que faltan datos en 2 columnas. Se eliminan las fechas conflictivas en todos los dataframes de cada una de las 35 empresas perdiendo un 6.8% de los datos.

## Búsqueda del comparador
El valor encontrado que mejor resume cada gráfica es el valor de retorno o return que mide el % de cambio respecto del valor que poseía el día anterior.

## Conclusiones
A partir de las correlaciones obtenidas y exigiendo un mínimo de .7 de correlación se agrupan las empresas obteniendo:

Grupo 1: BBVA, BKT, CABK, SABE, SAN.

Grupo 2: ENAG, REE.

Grupo 3: MAP, SAN.

Grupo 4: TEF, SAN.

Grupo 5: BBVA, BKT, CABK, SABE, SAN, TEF, MAP.

El primero contiene los bancos con relaciones más fuertes entre sí (BBVA, Bankinter, CaixaBank, Sabadell y Santander). El Santander (SAN) extiende su influencia a otros grupos, teniendo relaciones en 3 y 4 con Mapfre (MAP) y  Telefónica (TEF), el quinto grupo es el conjunto de todas las relaciones de este banco. Dejando de lado a los bancos, el grupo 2 contiene dos empresas relacionadas con la energía.

Relajar más el umbral de correlación provoca que se vayan completando los grupos, provando la hipótesis inicial.
