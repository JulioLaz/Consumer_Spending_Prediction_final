![ingresos_subcontinent_pie](https://github.com/JulioLaz/Consumer_Spending_Prediction_final/assets/108642139/f9105af0-89f5-48d1-8b04-500244b90254)CONSUMER SPENDING PREDICTIONS

![image](https://github.com/JulioLaz/Consumer_Spending_Prediction_final/assets/108642139/083209f5-14ed-45c5-bf9c-3ac57794dae1)

PROBLEMA DE NEGOCIO


La necesidad de prever y optimizar el gasto de sus usuarios ha llevado a una empresa de comercio electrónico a buscar soluciones innovadoras. Como científicos de datos, hemos sido convocados para desarrollar un modelo de machine learning que pueda predecir con precisión cuánto gastará un usuario al visitar dicho sitio web.


Tareas a realizar:


Preprocesamiento de Datos: Importar correctamente y analizar y comprender el conjunto de datos proporcionado, realizar limpieza de datos, eliminar atributos que no aportan valor y manejar valores faltantes.

Exploración y Feature Engineering: Realizar visualizaciones para entender las relaciones entre las variables y seleccionar las características relevantes, identificar variables llaves, codificación de variables categóricas y normalización/escalado de datos.

Construcción de Modelos: Experimentar con algunos algoritmos de machine learning como Linear Regression, Random Forest Regressor, Light GB, XGBoost, entre otros.

Evaluación y Selección del Modelo: Evaluar los modelos utilizando métricas como el error cuadrático medio (MSE), la raíz cuadrada del error cuadrático medio (RMSE) y el coeficiente de determinación (R²). Seleccionar el modelo con el mejor rendimiento para la predicción del gasto de los usuarios.

![pie_revenue_count](https://github.com/JulioLaz/Consumer_Spending_Prediction_final/assets/108642139/5bf0ce56-23b6-4bf8-9dcc-56dbe73cd2ed)

La variable objetivo o target, conocida como 'transaction revenue', exhibe una distribución altamente sesgada, donde aproximadamente el 98.7% de las observaciones tienen un valor de cero, mientras que solo el 1.3% restante corresponde a valores mayores que cero. Este desequilibrio en la distribución de la variable sugiere que la gran mayoría de las transacciones registradas no generaron ingresos, lo cual puede ser un indicativo relevante a considerar en el análisis y modelado de datos. Es importante abordar este desbalance durante el proceso de modelado para evitar sesgos y asegurar que el modelo pueda generalizar adecuadamente para predecir casos con ingresos significativos.

Porcentaje de ingresos de Transacciones continente
![ingresos_subcontinent_pie](https://github.com/JulioLaz/Consumer_Spending_Prediction_final/assets/108642139/03ce66fd-3d6e-4c89-ac0e-2815a9fd540e)

Ingresos de Transacciones por país y continente

![ingresos_country_subcontinent (1)](https://github.com/JulioLaz/Consumer_Spending_Prediction_final/assets/108642139/be64c29e-2933-4564-8ad3-59cfb14771e2)

Gráficas que nos ayudan a entender el problema planteado y también el análisis de algunas variables significativas

La gráfica tipo pie muestra la distribución de la variable target en relación a los ingresos por continentes, en la cual se destaca NorteAmérica con un 97,6% del total de los ingresos.

La gráfica tipo barras además de mostrar los continentes por colores, también nos muestra el país con mayores ingresos, Estados Unidos con alrededor del 97%.

![ingresos_operating_system](https://github.com/JulioLaz/Consumer_Spending_Prediction_final/assets/108642139/9ce20c50-c8fb-4f56-9313-d8a4be225e2b)

En esta gráfica observamos el sistema operativo que más se utilizó para ingresar a las páginas de compras. (graf. en escala log), En donde Macintosh supera casi por 10 veces al Windows y Chrome OS. Los usuarios que utilizan Macintosh suelen ser aquellos que prefieren los productos de Apple y los equipos suelen ser más costosos.

![ingresos_browser_operationsystem (1)](https://github.com/JulioLaz/Consumer_Spending_Prediction_final/assets/108642139/06dd1145-19d7-456d-a1eb-e7f36f745c1a)

El navegador Chrome en equipos Macintosh supera por casi 10 veces al resto. Chrome es conocido por su rendimiento rápido y su amplia compatibilidad con una variedad de plataformas y sistemas operativos. Los usuarios de Macintosh pueden optar por Chrome debido a su experiencia de navegación fluida y consistente en sus dispositivos.

Ingresos de Transacciones en relación al horario de compras

![ingresos_time_range (1)](https://github.com/JulioLaz/Consumer_Spending_Prediction_final/assets/108642139/33789180-7cfc-44b8-b816-d28b022c0b19)
![ingresos_time_range_pie (1)](https://github.com/JulioLaz/Consumer_Spending_Prediction_final/assets/108642139/bd8e0579-dfae-4a3d-931b-ac07bd383834)

Es interesante observar que los mayores ingresos por compras se realizaron durante la tarde-noche, en donde ambas superan el 86% del total.


Gráfico de dispersión de la variable Transaction Revenue
![scatter_revenue (1)](https://github.com/JulioLaz/Consumer_Spending_Prediction_final/assets/108642139/2cbc942c-0aa2-4a8a-9388-d45689be66cb)

En la gráfica se observa una línea en color rojo que representan los 21119 puntos solapados con valor de transaction revenue iguales a ceros, y los puntos por arriba de la línea son los 164 > 0. Se observa que por arriba de los 300 comienzan los puntos aislados (outliers).

Distribución de la variable Transaction Revenue el muestreo es sólo con valores >0
![ingresos_boxplot_revenue (1)](https://github.com/JulioLaz/Consumer_Spending_Prediction_final/assets/108642139/98bcbef9-ab0c-44a1-b344-525a2201d372)

En la gráfica observamos que la media y la mediana están alejadas por lo que su distribución no es simétrica (está sesgada). Los bigotes se distribuyen el inferior desde 0 y el superior 250 aprox. Se quitaron los ceros, porque de lo contrario la gráfica sólo mostraría una línea en ceros y el resto serían outliers, ya que la proporción de ceros es de 98.7%.

Mapa de correlaciones con valores > 10%
![corr_10up](https://github.com/JulioLaz/Consumer_Spending_Prediction_final/assets/108642139/633c96c0-6e3d-4cd7-b87a-aa2f9e759fac)

Observamos que existen correlaciones cercanas al 100% entre algunas variables, lo que indica una alta redundancia en la información proporcionada por esas variables. En este contexto, es importante analizar si estas variables aportan valor significativo al modelo predictivo o si, por el contrario, pueden introducir ruido o duplicar la información. En caso de que las variables altamente correlacionadas no aporten información adicional relevante, puede ser conveniente eliminarlas del modelo para evitar problemas de multicolinealidad y mejorar su interpretabilidad y generalización.

Análisis de las métricas de los modelos entrenados
![grafica_metrics_00 (1)](https://github.com/JulioLaz/Consumer_Spending_Prediction_final/assets/108642139/37360ecd-fc2c-433e-aaa8-84e58f7eadba)

El mejor valor de R2 es el mayor porque indica un mejor ajuste del modelo a los datos y una mayor capacidad del modelo para explicar la variabilidad en los datos observados.

Después de evaluar los resultados de los diferentes modelos de regresión, podemos sacar las siguientes conclusiones finales:


Observamos que tanto LightGBM como XGBoost superan significativamente el rendimiento de los otros dos modelos en todas las métricas evaluadas (R2, RMSE y MSE). Esto indica que estos modelos son más efectivos para capturar la variabilidad en los datos y generar predicciones más precisas.

La Regresión Lineal y Random Forest muestran un rendimiento inferior en comparación con LightGBM y XGBoost. Esto podría deberse a que estos modelos son menos flexibles y no pueden capturar la complejidad de los datos de manera tan efectiva como los modelos de gradient boosting como LightGBM y XGBoost.


Tabla comparativa del valor real de la variable target: transactionRevenue y los resultados de las predicciones de los modelos LightGB y XGB con sus respectivas variaciones ‘deltas’ respecto de la variable objetivo.
![image](https://github.com/JulioLaz/Consumer_Spending_Prediction_final/assets/108642139/93bbc7c2-d1ee-4193-8811-6ed94c950ee1)

Observamos que los deltas de XGB tienen menor variación, lo que indica que tiene mejor exactitud en las predicciones


Por lo tanto, sabiendo que LightGBM y XGBoost tienen los mejores R2, y aunque XGBoost tiene un RMSE ligeramente mayor, su R2 es ligeramente mejor que LightGBM. Sin embargo, la diferencia en el rendimiento entre los dos modelos es mínima. Por lo tanto, la elección entre LightGBM y XGBoost puede depender de otros factores como la facilidad de implementación o la interpretación del modelo.

Elección de modelos:

Aunque los rendimiento de LightGBM y XGBoost superan a los de la Regresión Lineal y Random Forest, recomendaremos XGBoost para la predicción de los valores de transactionRevenue. Este modelo proporciona una mejor capacidad predictiva y es más adecuado para manejar la complejidad de los datos. Queda clara la superioridad de XGBoost al comparar la suma de los deltas respecto a los valores reales y predichos: de la muestra total (164 transaction revenue) XGBoost se aleja un 37% de los valores reales, ante un 63% del modelo LightGBM.


Gráfico de Líneas de predictions XGB - Líneas Verticales de los Deltas
![grafica_plot_original_s_nota (2)](https://github.com/JulioLaz/Consumer_Spending_Prediction_final/assets/108642139/800c65b9-4315-4161-948e-253e3c4582ee)

Suma total de las diferencias de deltas en XGB: 6592
representa un 37.28% de la sum(target)=17681
total de muestras: 164
Observando la amplitud de las líneas verticales, éstas representan cuánto se alejan del valor real.

Gráfico de barras representando las variaciones deltas de la gráfica anterior, cuyos valores se observan en el eje x.
![grafica_deltas_origina_01_sin notas (1)](https://github.com/JulioLaz/Consumer_Spending_Prediction_final/assets/108642139/ae89a65d-20bc-4c37-b2d7-a6e01f702e7e)

Las barras expresan la variación de la predicción respecto del valor real. En el eje x observamos los valores reales de la variable objetivo arriba, y abajo se observan los valores predichos. Observamos el valor medio= 27.2

Gráfico de predictions XGB con factor de corrección
![grafica_plot_factor_s_nota (1)](https://github.com/JulioLaz/Consumer_Spending_Prediction_final/assets/108642139/10d4ff8f-c29c-421b-8ebf-e8a26d9fae8a)
Suma total de las diferencias: 5263
representa un 29.77% de la sum(target)=17681
total de muestras: 164
Observamos una mejor aproximación corrigiendo un 7% respecto del modelo anterior.

Gráfico de barras representando las variaciones deltas de la gráfica anterior con factor de corrección
![grafica_deltas_factor_s_titulos (2)](https://github.com/JulioLaz/Consumer_Spending_Prediction_final/assets/108642139/58ce4332-1221-4645-9b79-d12550cf492a)
Observamos el valor de la media= 15.02, con lo cual se produce una mejora del valor medio de las predicciones de un 45% respecto de la media sin factor de corrección (media=27.2)

Conclusión

Después de realizar un exhaustivo proceso de preprocesamiento y feature engineering en los datos de tráfico del sitio, he logrado transformar y enriquecer el conjunto de datos para su posterior análisis y modelado.

En el preprocesamiento, llevé a cabo acciones como la limpieza de datos, la conversión de tipos de datos, la eliminación de columnas con un solo valor y el manejo de valores nulos. Además, desempaqué las columnas de diccionario, apliqué codificación de etiquetas y dividí la columna 'visitStartTime' en varias características temporales útiles.

En el feature engineering, creé nuevas características derivadas de las existentes, como la categorización del tiempo, la identificación de los principales navegadores y meses, y la codificación de la frecuencia para ciertas columnas. También optimicé la memoria del dataframe para mejorar la eficiencia del análisis.

Luego de explorar patrones, identificar correlaciones y construir modelos. Se evaluaron los resultados de los mismos, se seleccionó XGBoost por su mejor respuesta predictiva (ver análisis anterior).

Esto es una primera aproximación para dar respuesta objetiva a la necesidad de predecir y optimizar el gasto de los usuarios.

El modelo XGBoost (o los modelos) puede mejorar su capacidad predictiva aumentando el coeficiente de determinación R2. Esto es parte de mi desafío  como Data Scientist!

Julio A. Lazarte
https://www.linkedin.com/in/julio-lazarte-developer/
