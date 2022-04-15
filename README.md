
# Segmentación de clientes

<span>La segmentación de clientes es el proceso que permite a las empresas dividir a sus consumidores en categorías específicas, basadas en características que se extraen de su comportamiento como clientes y la información que pueden obtener de sus interacciones con la empresa.</span>

Para este proyecto de <b>segmentación de clientes</b>, se usará un algoritmo de aprendizaje no supervisado, <b>k-means</b>; el cual, es un método de agrupamiento, que tiene como objetivo la partición de un conjunto de n observaciones (clientes en este caso) en k cantidades de segmentos, en el que cada observación o cliente quedará clasificado en uno de estos grupos. 

La base de datos que se usará para la elaboración de este cuaderno fue tomado de Kaggle: 
<a href="https://www.kaggle.com/vjchoudhary7/customer-segmentation-tutorial-in-python">Dataset</a>

### Dataset
<img src="https://github.com/PabloJRW/segmentacion_de_clientes/blob/main/img/data.png"/>

Para esta tarea contamos con un conjunto de datos de 5 variables.
>>>><li> <b>CustomerID:</b> identificador único de los clientes.
>>>><li> <b>Gender:</b> género de los clientes. (Male, Female)
>>>><li> <b>Age:</b> edad de los clientes.
>>>><li> <b>Annual Income:</b> ingreso de los clientes por año.
>>>><li> <b>Spending Score (1-100):</b> puntuación de compra. 
    
K-Means encuentra clústers basándose en la distancia, por lo que es importante que sólo utilizemos variables numéricas. También, excluiremos la variable <b>"CustomerID"</b>, debido que sólo es un identificador que no nos aportará información. Nos quedamos con 3 variables.
#### Distribución original:
<img src="https://github.com/PabloJRW/segmentacion_de_clientes/blob/main/img/distributions.png"/>
A estas variables le aplicamos un método de normalización. 
    
### Elegir K (Cantidad de clusters)
Cuando no tenemos una cantidad de segmentos en la que queramos clasificar nuestros datos, o queramos descubrir cuántos grupos similares tenemos en nuestros datos, el método de codo es el apropiado para ayudarnos a tomar esa decisión.
    
<img src="https://github.com/PabloJRW/segmentacion_de_clientes/blob/main/img/elbow_viz.png"/>
Mediante el método de codo podemos observar que entre nuestros datos existen entre 4 y 6 segmentos de clientes bien definidos. Este es un punto donde entra el criterio experto para tomar la decisión de cuántos segmentos debemos establecer. El método de codo nos sugiere 4 clusters.
    
#### Visualización de los 4 clusters
<img src="https://github.com/PabloJRW/segmentacion_de_clientes/blob/main/img/cluster_4k.png"/>

#### Visualización de los 5 clusters
<img src="https://github.com/PabloJRW/segmentacion_de_clientes/blob/main/img/cluster_5k.png"/>    
    
### Conclusión
Como se menciona anteriormente, la cantidad de segmentos o clusters k es definido mediante criterio experto, el cual podría depender del problema al cual se busca hallar una solución. O bien, podríamos utilizar el método de codo para casos en el cual no tengamos una tarea definida o estemos desarrollando minería de datos.
 

