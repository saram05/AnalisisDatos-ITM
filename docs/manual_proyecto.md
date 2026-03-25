# Manual del Proyecto

Este proyecto se desarrolló con el objetivo de analizar el comportamiento de los clientes a partir del dataset *Customer Personality Analysis*. La idea principal fue entender cómo se relacionan variables como el ingreso, el gasto y algunas características demográficas, y dejar los datos listos para un posible modelo de segmentación.

Primero se hizo una exploración general para entender la estructura del dataset y elegir el más adecuado. Luego, en el análisis exploratorio, se revisaron valores faltantes, distribuciones y relaciones entre variables. En esta parte se identificaron algunos problemas como edades poco realistas y valores muy altos en ingresos, además de una relación clara entre ingreso y gasto.

Con base en eso, se pasó al preprocesamiento. Se creó la variable edad a partir del año de nacimiento, se completaron los valores faltantes en ingresos usando la mediana y se eliminaron los datos que podían afectar el análisis, como outliers y columnas que no aportaban información relevante. También se transformaron las variables categóricas para poder trabajar con ellas numéricamente y se escalaron los datos, ya que esto es necesario para aplicar PCA correctamente.

Finalmente, se utilizó PCA para reducir la cantidad de variables. Primero se analizó cuánta varianza explicaban los componentes y luego se redujo a dos dimensiones para poder visualizar los datos. Esto permitió tener una idea general de cómo se distribuyen los clientes y dejó el dataset listo para aplicar técnicas de clustering en una siguiente fase.

En general, el proceso fue consistente entre etapas, ya que cada decisión tomada en el preprocesamiento se basó en lo encontrado en el análisis exploratorio.
