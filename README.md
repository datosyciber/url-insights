# url-insights
En este documento se explica en profundidad los aspectos más teóricos de los modelos utilizados para determinar cuáles son las características que ayudan a reconocer y clasificar un enlace como malicioso o benigno.

## Árbol de decisión

Un árbol de decisión es un algoritmo de aprendizaje supervisado no paramétrico, que se utiliza tanto para tareas de clasificación como de regresión. Tiene una estructura jerárquica de árbol, que consta de un nodo raíz, ramas, nodos internos y nodos hoja.

- no paramétrica = se presupone que la distribución de la que proviene la muestra no está especificada, o dicho en otras palabras, no hace suposiciones explícitas sobre la forma funcional de la relación que está intentando aproximar.
- modelo supervisado = aprende a predecir resultados basándose en datos de entrada etiquetados.

Un árbol de decisión comienza con un nodo raíz, que no tiene ninguna rama entrante. Las ramas salientes del nodo raíz luego alimentan los nodos internos, también conocidos como nodos de decisión. En función de las características disponibles, ambos tipos de nodos realizan evaluaciones para formar subconjuntos homogéneos, que se denotan mediante nodos hoja o nodos terminales. Los nodos hoja representan todos los resultados posibles dentro del conjunto de datos.

En el caso de que generemos un modelo demasiado complejo, se puede llevar al sobreajuste de los datos, por lo que en muchos casos el conveniente conservar la simplicidad en las predicciones (principio de parsimonia de la Navaja de Occam) y realizar la poda, es decir, reducir la complejidad eliminando las ramas cuyas características utilizadas son menos relevantes para la predicción.

La **impureza de Gini*** es la probabilidad de clasificar incorrectamente un punto de datos aleatorio del conjunto de datos si se etiquetara en función de la distribución de clases del conjunto de datos. Cuanto más cercano sea su valor a cero, entonces más pura será la clase.

Una de las grandes ventajas de este modelo es que no requiere una exigente preparación de los datos, acepta valores discretos o continuos, y los valores continuos se pueden convertir en valores categóricos mediante el uso de umbrales, e incluso valores faltantes. Uno de los inconvenientes más relevantes de este modelo es que tiende al sobreajuste, por lo que hay que como se comentaba anteriormente, es mejor mantener la simplicidad para evitar que esto ocurra.

## Regresión legística



### Fuentes
[1] https://www.ibm.com/es-es/think/topics/decision-trees
