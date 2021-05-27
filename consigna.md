#### Recursos
Utiliza los siguientes recursos para realizar el proyecto:

Notebook de Jupyter(resuelto en archivo ipynb)

Dataset Properati: https://drive.google.com/uc?export=download&id=1Ugbsw5XbNRbglomSQO1qkAgMFB_3BzmB


### Consigna

#### PARTE 1 - Pensando como un/a Data Scientist

##### Problema
Recientemente te has incorporado al equipo de Datos de una gran inmobiliaria. La primera tarea que se te asigna es ayudar a los tasadores/as a valuar las propiedades, ya que es un proceso difícil y, a veces, subjetivo. Para ello, propones crear un modelo de Machine Learning que, dadas ciertas características de la propiedad, prediga su precio de venta.

#### PARTE 2 - Análisis Exploratorio de Datos

En esta sección, te proveeremos de un Dataset relacionado con la problemática planteada para que realices un Análisis Exploratorio de Datos. Deberás responder las preguntas típicamente asociadas a este análisis para obtener una primera descripción del Dataset.

#### PARTE 3 - Primer Modelo de Machine Learning

Una vez explorado el dataset, deberás utilizar herramientas de Machine Learning para predecir la variable de interés. Para ello, tendrás que:

1) Elegir la métrica que utilizarás para evaluar las predicciones.
2) Generar tres modelos: un modelo Benchmark, un modelo basado en Vecino más Cercanos (Modelo 1) y otro basado en Árboles de Decisión (Modelo 2). Cada uno de estos modelos deberá ser correctamente entrenado y evaluado siguiendo un flujo de trabajo típico de Machine Learning (train/test split).
3) Optimizar el desempeño de los Modelos 1 y 2 optimizando el número de vecinos y la profundidad del árbol, respectivamente.
4) Comparar la performance de los Modelos 1 y 2 frente al modelo Benchmark y entre sí para decidir cuál modelo tiene mejor desempeño.

### Checklist de evaluación

##### PARTE 1 - Pensando como un/a Data Scientist

Debes justificar por qué creés que los datos que elegiste ayudan a resolver la problemática planteada.

##### PARTE 2 - Análisis Exploratorio de Datos

Debes responder las preguntas típicas de un Análisis Exploratorio de Datos.
Debes utilizar histogramas para representar la distribución de variables numéricas, gráficos de barras para variables categóricas y diagramas de dispersión para visualizar la relación entre dos variables numéricas. Si no exploras alguna variable (columna), deberás justificar por qué.
Los gráficos deben estar correctamente presentados, con título y etiquetas en cada eje. Cada gráfico debe ir acompañado de una breve descripción. Si existen valores atípicos que distorsionan la visualización de un gráfico, el límite de cada eje debe estar ajustado para que esto no suceda o el dataset debe ser filtrado.

##### PARTE 3 - Primer Modelo de Machine Learning

La elección de la métrica de evaluación debe estar correctamente justificada.
Debes elegir correctamente las variables predictoras y la variable a predecir.
Realiza un train/test split de los datos.
El modelo benchmark debe estar justificado y evaluado de forma similar a los modelos generados.
Debes justificar cuál modelo elegirías para utilizar.
Debes ser crítico/a con la metodología utilizada. ¿Qué mejorarías?
