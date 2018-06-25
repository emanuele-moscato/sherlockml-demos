# Table of contents

This project contains various demos for SherlockML. The files in the `project/` folder were already there and are mostly related to the Customer Intelligence demo and to using the Opendata library. They will be left there for now so that people already used to showing them can still find them.

If you want to create new demos/project/files, please create a suitably named folder under `project/` and work in there.

The other folders contain:
- `anomaly-detection/`: a demo on anomaly detection based on a [Kaggle challenge](https://www.kaggle.com/c/anomaly-detection-challenges) and using gradient boosted trees (XGBoost) and a simple neural network built with Keras.

- `apis/`: contains the "Cat vs dog person" demo API, along with a Jupyter notebook to test it.

- `App/`: contains files to run Apache Airflow as a SherlockML web app.

- `apps/`: contains files to run various web apps. See below for a detailed list.

- `clustering-demo/`: contains a demo on dimensional reduction and clustering (the data is randomly generated). Also includes an API and a web app: the former serves the data and the latter is a dashboard for visualisation and clustering.

- `customer-intelligence`: 
    - `Customer_intelligence_usage.ipynb`: demo on Customer Intelligence, using the `customerintelligence` and the `opendata` modules from the `sherlockml` library.
    - `CI_report.ipynb`: notebook that shows how to create a report with customer numbers, UK postcodes on a geographical map and stock market data (with an interactive widget built using Plotly). Interesting to show how to use the `opendata` library, how to have interactive output and how to put all this into a report.
    - `Using_open_data.ipynb`: notebook that shows how to use the `opendata` library, loading census data for UK output areas and then, extracting some statistics and visualising areas on a map.

- `distributed-computing/`:
    - `connecting/`: Jupyter notebooks showing how to connect to Hive, Impala and Spark services (they can't be run as they try to connect to services that are not active, but can be useful for people to see how it is done on SherlockML).
    - `spark-local/`: files and a bash script needed to run Spark locally on a SherlockML server. This is taken from the fellowship workshop on distributed computing.

- `influxdb/`: contains a Python package to install the InfluxDB database, run it locally on a SherlockML server and connect to it via a Python client, as shown in the relative notebook. To install and run InfluxDB, apply the `install-influxdb` environment or execute the `install-influxdb.sh` script in the same folder.

- `nlp_project/`: an NLP demo on audio transcription based on Mozilla's DeepSpeech model and on the Amazon Transcribe API. The data is also hosted in Datasets. An app can be run to upload audio files and transcribe them with DeepSpeech.

- `other/`: various files, again on Customer Intelligence, connecting to databases and using the `slackclient` Python libary to get alerts on Slack.

- `postgrasql_db/`: contains code to run a PostgreSQL database locally on a SherlockML server (execute the `install-postgresql.sh` script) and connect to it via a Jupyter notebook. This is done using `psycopg2` and `sqlalchemy` and also demonstrates how to get a Python connection object that reads a hidden files containing the credentials.

## Available apps
Web apps available in the `/project/apps/` folder (all already present in the Deployments section):
- `airflow/:` runs Apache Airflow as a SherlockML web app.

- `customer-intelligence/`: app that simply redirects to the Customer Intelligence web page.

- `dash-uber-rides-demo/`: classic Plotly Dash demo app that creates a dashboard representing Uber rides in New York.

- `london-cycle-flow/`: creates a dashboard with a 3D plot of data from the bicycle sensors TFL has around London. A linear regression is performed and the user can specify new datapoint for which to make a prediction.

- `tfl-count-entries/`: app that simply represents the number of entries versus time of that day in different London tube stations. A button allows to visualise data for more stations and send a Slack alert at the same time.