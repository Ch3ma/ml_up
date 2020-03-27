##Instrucciones de uso.
Los archivos fuente se compartirán por google drive, por el peso de los archivos. Cada archivo hace referencia a un "path", que se instancia hacia la activación de drive sobre google colab, o una ruta específica de una máquina. Éste se deberá cambiar. 

Los archivos de feature extraction, toman entre 10 minutos y 9+ horas. Correr con precaución.

##Orden para correr el proyecto completo.

1) Archivos "Feature Extraction".
	-II, IIA, IIB, IV
2) Archivos ETL.
	-ETL I, ETL II, ETL III, ETL IV, ETL V
3) Modelado 
	-Modelling I A, Modelling I B, Modelling II.
	
### <span style="color:blue"> NOTA Si se desea saltar la fase de extracción de datos y "feature engineering" y se desea ver desde el muestreo hasta el modelado y prueba, revisar desde el archivo ETL V en adelante.</span>

### Descripción
Este repositorio es la entrega del trabajo final para la clase de ML en universidad panamericana. Código fuente para "Detección de insiders utilizando metodologías de Machine Learning" por Ulises Jiménez y José María Sarmiento.

### Lista de archivos
Se listan los archivos dentro del repositorio con su descripción

| Notebook | Descripción |
| ------ | ------ |
| [Feature extraction II](InsiderTrading_feature_extraction_part_II.ipynb) | En este archivo se generan los features relacionados al sentimiento de http y email, los salarios, las fechas de inicio y salida de la empresa, el acceso a archivos y el uso de dispositivos de almacenamiento |
| [Feature Extraction III A] (InsiderTrading_feature_extraction_part_III_A.ipynb) | Lee los emails y clasifica el tipo del dominio. |
| [Feature Extraction III A] (InsiderTrading_feature_extraction_part_III_B.ipynb) | Lee la actividad web del protocolo http y clasifica el tipo de dominio. |
| [Feature Extraction IV] (InsiderTrading_getDomiansClass.ipynb) | Unifica los archivos generados con la clasificación de dominios de email y http y genera un archivo unificado para la creación del data mart. |
| [Etl I](InsiderTrading_etl_part_I.ipynb) | Creación de la primera parte de la fuente final de datos, en este archivo se leen los archivos relacionados con comportamiento de archivos, sentimiento web y http |
| [ETL II](InsiderTrading_etl_domians_gender_insiderCases.ipynb) | Archivo donde extrae la clasificación de los dominios a partir de los URL, se generan las etiquetas de género a partir del primer nombre y se genera la primer parte del "data mart" para insiders. |
| [Etl III] (InsiderTrading_feature_extraction_log_activity.ipynb) | En este archivo se toma el comportamiento en el sistema a partir de su actividad de accesos. |
| [Etl IV](InsiderTrading_etl_part_II.ipynb) | Creación de la segunda parte de la fuente final de datos, en este archivo se leen los archivos relacionados con comportamiento en su actividad web, actividad en la empresa, variables calculadas de riesgo de insider y se genera la fuente final |
| [Etl V](InsiderTrading_etl_db_balance_sampling.ipynb) | Toma el "data mart", en este punto se generan las muestras Out of Sample y Out of Time y se balancea la muestra de entrenamiento. |
| [Modelling I A] (InsiderTrading_modelling_part_I_A.ipynb) | Archivo donde se genera el modelo Random Forest |
| [Modelling I B] (InsiderTrading_modelling_part_I_B.ipynb) | Archivo donde se genera el modelo Support Vector Machines |
| [Modeling II](InsiderTrading_modelling_part_II.ipynb) | Archivo donde se generan los modelos SGDClassifier y XGBoost |

