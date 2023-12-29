FROM python:3.8-slim-bullseye
ADD hb-ds-prod-key.json /hb-ds-prod-key.json

RUN apt-get update && apt-get -y install sudo
RUN apt-get install --reinstall -y build-essential
RUN apt-get install sshpass -y
RUN apt-get install libsasl2-dev -y

COPY src/ /{{cookiecutter.project_slug}}/src
COPY data/ /{{cookiecutter.project_slug}}/data
COPY models/ /{{cookiecutter.project_slug}}/models
COPY ./pyproject.toml /{{cookiecutter.project_slug}}
COPY ./poetry.lock /{{cookiecutter.project_slug}}
COPY ./ds_app.py /{{cookiecutter.project_slug}}
RUN mkdir /home/gcp_keys
COPY hb-ds-prod-key.json /home/gcp_keys/hb-ds-prod-key.json

WORKDIR /{{cookiecutter.project_slug}}

RUN pip install poetry
RUN poetry config virtualenvs.create false
RUN poetry install --no-dev
