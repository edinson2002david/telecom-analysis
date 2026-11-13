Análisis de datos de ConnectaTel
Objetivo
Analizar el comportamiento de los clientes de ConnectaTel con información registrada hasta 2024, para identificar patrones de uso, caracterizar a los usuarios, detectar valores atípicos y proponer oportunidades de mejora en los planes y estrategias de retención.
Datasets utilizados
El proyecto utiliza tres archivos CSV:
- plans.csv: información de los planes, como precios, minutos y GB incluidos, y costos por consumo adicional.
- users_latam.csv: información de los clientes, como edad, ciudad, fecha de registro, plan y fecha de cancelación (churn).
- usage.csv: registros de uso de los servicios, incluidas llamadas y mensajes.
Los archivos CSV deben estar disponibles para que el notebook pueda cargarlos. No se asume que estén incluidos en este repositorio.
Etapas del análisis
1. Carga y exploración: lectura de los datasets, revisión de dimensiones, columnas y tipos de datos.
2. Calidad de datos: identificación de valores nulos, valores inválidos, sentinels y revisión de fechas.
3. Limpieza: tratamiento de -999 en age, reemplazo de ? en city por un valor nulo y revisión de fechas fuera de rango. Los nulos de duration y length se mantienen porque dependen del tipo de registro (type).
4. Resumen por usuario: agregación de mensajes, llamadas y minutos de llamadas por user_id, y combinación con la información de clientes.
5. Análisis exploratorio: estadísticas descriptivas, distribución de planes, histogramas y detección de valores atípicos mediante diagramas de caja y el método IQR.
6. Segmentación: clasificación de clientes por nivel de uso (Bajo uso, Uso medio y Alto uso) y por edad (Joven, Adulto y Adulto Mayor).
7. Insight ejecutivo: síntesis de hallazgos y recomendaciones para los stakeholders.
Tecnologías
- Python
- pandas
- NumPy
- Matplotlib
- Seaborn
- Google Colab / Jupyter Notebook
