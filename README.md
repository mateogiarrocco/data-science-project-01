# Primer modelo de Machine Learning (Proyecto n°1)

### Resumen del proyecto
##### Este proyecto te desafía a seleccionar una problemática entre un conjunto de opciones, indagar qué datos podrían ayudarte a abordarla, realizar un análisis exploratorio y entrenar un modelo sencillo de Machine Learning para resolverla. ¡Esperamos que puedas llevar adelante un primer flujo de trabajo tal como lo hacemos los/as Data Scientists!

#### Recursos
Utiliza los siguientes recursos para realizar el proyecto:

Notebook de Jupyter: https://colab.research.google.com/drive/1b9lR64M8_dnIBKQ95zRscMmrXsJ3qv05

Dataset Properati: https://drive.google.com/uc?export=download&id=1Ugbsw5XbNRbglomSQO1qkAgMFB_3BzmB


#### Consigna

#### PARTE 1 - Pensando como un/a Data Scientist

##### Problema
Recientemente te has incorporado al equipo de Datos de una gran inmobiliaria. La primera tarea que se te asigna es ayudar a los tasadores/as a valuar las propiedades, ya que es un proceso difícil y, a veces, subjetivo. Para ello, propones crear un modelo de Machine Learning que, dadas ciertas características de la propiedad, prediga su precio de venta.

En esta sección, te planteamos una problemática y deberás responder la siguiente pregunta:
¿Qué datos crees que te ayudarían a trabajar en el problema? ¿Por qué?
Importante: NO deberás buscar esos datos, solamente justificar qué información crees que te ayudaría a resolver la problemática planteada.

#### PARTE 2 - Análisis Exploratorio de Datos

En esta sección, te proveeremos de un Dataset relacionado con la problemática planteada para que realices un Análisis Exploratorio de Datos. Deberás responder las preguntas típicamente asociadas a este análisis para obtener una primera descripción del Dataset.

Debes realizar un Análisis Exploratorio de Datos sobre el dataset de propiedades de Properati. Es importante que respondas las siguientes preguntas durante el análisis:

¿Qué tamaño tiene el dataset?¿Cuántas instancias y cuántas columnas?
¿Cuántos valores faltantes hay en cada columna?
¿Cómo es la distribución de cada variable? Deberás hacer histogramas para las variables numéricas y gráficos de barras para las variables categóricas.
¿Cómo se relacionan las variables entre sí?¿Qué tipo de gráfico será conveniente para presentar esta información?
¿Cómo están correlacionadas las variables numéricas?¿Qué tipo de gráfico será conveniente para presentar esta información?¿Cuáles serán los mejores predictores de la variable de interés?


Importa las librerías necesarias para trabajar en la consigna.
1. Carga el dataset usando las funcionalidades de Pandas. Imprimir cuántas filas y columnas tiene, y sus cinco primeras instancias.
2. Valores Faltantes: imprime en pantalla los nombres de las columnas y cuántos valores faltantes hay por columna.
3. Tipos de propiedad: ¿Cuántos tipos de propiedad hay publicados según este dataset?¿Cuántos instancias por cada tipo de propiedad hay en el dataset? Responde esta pregunta usando las funcionalidad de Pandas y con un gráfico apropiado de Seaborn. Pistas: Te puede ser útil googlear cómo rotar las etiquetas del eje x.
4. ¿De qué regiones son las publicaciones? Haz gráficos de barras para las variables l2 y l3. Si te animas, puedes hacer los dos gráficos usando subplot de Matplotlib. Dale un tamaño apropiado a la figura para que ambos gráficos se visualicen correctamente.
5. Filtrando el Dataset: A partir de los resultados del punto 3. y 4., selecciona las tres clases más abundantes de tipos de propiedad y la región con más propiedades publicadas. Crea un nuevo Data Frame con aquellas instancias que cumplen con esas condiciones e imprime su shape.
`Checkpoint`: deberías tener un dataset con 91485 instacias, 19 columnas.

6. Distribuciones y relaciones de a pares: Estudia la distribución y las relaciones de a pares de las variables rooms, bedrooms, bathrooms, surface_total, surface_covered, price para cada tipo de propiedad. Para ello, ten en cuenta:
A) Obtiene estadísticos que te sirvan para tener una primera idea de los valores que abarcan estas variables. ¿Cuáles crees que toman valores que tal vez no tengan mucho sentido?
B) Algunas instancias tienen valores de superficie (surface_total) muy grandes y dificultan la correcta visualización. Estudia la distribución de esa variable y filtra por un valor razonable que te permita obtener gráficos comprensibles. Puede ser útil un boxplot para determinar un rango razonable.
C) Lo mismo ocurre con valores de superficie total muy chico.
D) Las propiedades no pueden tener surface_covered mayor a surface_total. Si eso sucede, debes filtrar esas instancias.
E) El rango de precios que toman las propiedades es muy amplio. Estudia la distribución de esa variable y filtra por un valor razonable que te permita obtener gráficos comprensibles. Puede ser útil un boxplot para determinar un rango razonable.
F) Una vez filtrado el dataset, puedes utilizar la función pairplot de Seaborn.
7.Correlaciones: Estudia la correlación entre las variables rooms, bedrooms, bathrooms, surface_total, surface_covered, price. ¿Cuáles son las mejores variables para predecir el precio?¿Qué diferencias encuentras según cada tipo de propiedad?

##### 2.1 Desafío
En el dataset provisto hay mucha información, más allá del problema planteado. Propone una pregunta que pueda ser respondida por el dataset e intenta responderla.¿Cuáles son los sesgos de la respuesta obtenida?(¿Cuán generalizable es la respuesta obtenida?)¿Necesitas información complementaria?¿Cómo la obtendrías?

Por ejemplo: ¿Cuál es el barrio más caro de Buenos Aires? Probablemente puedas responder esta pregunta con este dataset. Pero podria ocurrir que la respuesta esté sesgada. ¿Cómo? Tal vez las propiedades más caras no se publican de forma online, sino que utilizan otro canal de venta.

#### PARTE 3 - Primer Modelo de Machine Learning

Una vez explorado el dataset, deberás utilizar herramientas de Machine Learning para predecir la variable de interés. Para ello, tendrás que:

1) Elegir la métrica que utilizarás para evaluar las predicciones.
2) Generar tres modelos: un modelo Benchmark, un modelo basado en Vecino más Cercanos (Modelo 1) y otro basado en Árboles de Decisión (Modelo 2). Cada uno de estos modelos deberá ser correctamente entrenado y evaluado siguiendo un flujo de trabajo típico de Machine Learning (train/test split).
3) Optimizar el desempeño de los Modelos 1 y 2 optimizando el número de vecinos y la profundidad del árbol, respectivamente.
4) Comparar la performance de los Modelos 1 y 2 frente al modelo Benchmark y entre sí para decidir cuál modelo tiene mejor desempeño.
