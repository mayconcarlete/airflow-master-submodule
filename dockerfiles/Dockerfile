FROM apache/airflow:2.5.1-python3.10 AS base

RUN pip3 install poetry

COPY ../pyproject.toml .

RUN poetry install --no-root --no-interaction --no-ansi --only main

ARG ROOT_PATH=/opt/airflow
WORKDIR ${ROOT_PATH}
RUN ls
# lembrar de adicionar as dags e tudo no python path
# ENV PYTHONPATH=${PYTHONPATH}:${ROOT_PATH}/dags:${ROOT_PATH}/plugins