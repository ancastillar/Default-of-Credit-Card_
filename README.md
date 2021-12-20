# Análisis del incumplimiento de pago: Tarjetas de crédito

En objetivo de este proyecto es predecir la probabilidad de incumplimiento de una determinada obligación, en este caso tarjetas de crédito. Esto permitirá generar estrategias que minimicen el riesgo del deterioro de la salud financiera del cliente. Adicionalmente, con el fin de facilititar el desarrollo de las estrategias de cobranzas, se plantea emplear algoritmos de clusterización que permitan encontrar segmentos homogenéos dentro de la población y de esta manera dar un trato diferencial a cada cliente.

## Link para la aplicacion web https://defaultappnataliacastilla.herokuapp.com/
![plot](./imgs/web_app.PNG)
![plot](./imgs/web_app1.PNG)


## Sobre este repositorio
En este repositorio encontrarás todo lo necesario para reproducir mi trabajo

* notebooks: Encontrarás el código para reproducir todo.
* models: Están todos los modelos realizados
* imgs: Se encuentran todas las imágenes realizadas tanto en la exploración, preprocesamiento y clusterización
* data: Fuente de datos empleada: https://archive.ics.uci.edu/ml/datasets/default+of+credit+card+clients

## Model and results

Thirty-six classifiers were developed, using the Catboost algorithm. The lower metric was 0.70 
 and the upper metric was 0.93 AUC. You can check the results running the models (Please see the instructions).

### Instructions:

1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/models_clfs/ models/glove.6B.50d.txt`
    - *Please uncompress the file with glove embedding to running the models*
 
 
2. Run the following command in the app's directory to run your web app.
    `python app/run.py` or python/disaster_response_app.py

3. Go to http://0.0.0.0:3001/



## Prerrequisitos


* python3
* python packages in the requirements.txt file

Install the packages with

* pip install -r requirements.txt


