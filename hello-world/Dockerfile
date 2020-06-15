FROM python:3.6.3

ENV DEBIAN FRONTEND noninteractive

ENV TERM linux

                      
# Airflow setup      
                 
ENV AIRFLOW_HOME=/Airflow

RUN pip install apache-airflow
                    
COPY /dags/hello_world.py ${AIRFLOW_HOME}/dags/

copy airflow.cfg ${AIRFLOW_HOME}/airflow.cfg

copy /entrypoint.sh .

run chmod +x entrypoint.sh

EXPOSE 8080 5555 8793 

ENTRYPOINT ["/entrypoint.sh"]