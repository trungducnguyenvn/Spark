## Dataproc : Using web UI to submit the job
- Main Python file :
    gs://de-zoomcamp-week2-hw/script/spark_sql.py

- Parameter to the submit job:
 
   --input_green=gs://de-zoomcamp-week2-hw/Data/green/*/
   --input_yellow=gs://de-zoomcamp-week2-hw/Data/yellow/*/
   --output=gs://de-zoomcamp-week2-hw/Report



## Spark to BigQuery : Using web UI to submit the job

- Main Python file :
    gs://de-zoomcamp-week2-hw/script/spark_sql_bigquery.py


` Note : Using GCP SDK to submit the job : ` 

gcloud dataproc jobs submit pyspark \
    --cluster=cluster-17e3 \
    --region=asia-southeast1 \
    --jars=gs://spark-lib/bigquery/spark-bigquery-latest_2.12.jar \
    gs://de-zoomcamp-week2-hw/script/spark_sql_bigquery.py  \
    -- \
        --input_green=gs://de-zoomcamp-week2-hw/Data/green/*/  \
        --input_yellow=gs://de-zoomcamp-week2-hw/Data/yellow/*/ \
        --output=dataproc_bigquery.report