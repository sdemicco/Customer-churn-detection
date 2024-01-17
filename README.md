# Customer-churn-detection
Desarrollo de modelo machine learning para empresa productora de Packaging. Algoritmos de Clasificación en lenguaje Python. Proyecto integrador realizado en el marco de Digital House.

## Resumen


A partir de la necesidad de una empresa, se desarrolló un modelo que realiza predicciones ingresando datos de un cuatrimestre de ventas y obteniendo como resultado aquellos clientes no realizarán compras durante el año posterior al cuatrimestre.

El modelo realizado permite predecir la pérdida del cliente con una precisión del 89% y detecta el 69% de clientes propensos a perderse.

### Datos
***
:point_right:[enlace a notebook Datos](NOTEBOOKS/logistica-pipeline.ipynb)<br>
El modelo fue entrenado con datos de facturación desde 2019 hasta 2021. A partir de los campos del conjunto de datos original, se determinaron y calcularon las variables predictoras y el objetivo para el entrenamiento del modelo.

El enfoque cuatrimestral implicó un trabajo de preprocesamiento más importante, pero:
- Se aumentaron la cantidad de registros para el entrenamiento del modelo.
- Se obtuvo un modelo más versátil que solo necesita datos de 4 meses para realizar predicciones.

### Modelo de Clasificación
***
:point_right: [enlace a notebook modelo](NOTEBOOKS/modeling-pipeline.ipynb)<br>
Se probaron 6 algoritmos de clasificación. El criterio de selección del mejor algoritmo fue maximizar la precisión (minimizar falsos positivos) a costa de reducir a un nivel aceptable la detección de clientes propensos a perderse. Esto permite direccionar los recursos a los clientes que efectivamente dejarán de operar, a costa de detectar menos.

El modelo predictor permite identificar los atributos más importantes que afectan a la pérdida de clientes y poder actuar sobre los mismos. "Dólares por tonelada" y "Condición de pago" son, dentro de los más importantes, los que presentan margen de acción.

El modelo predictor desarrollado es una herramienta poderosa que le anticipa a la empresa la pérdida de un cliente, permitiéndole tomar las acciones necesarias en tiempo y forma para intentar revertir la pérdida.
