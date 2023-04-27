{% if cookiecutter.use_docker_hub_image=='yes' %}
FROM {{ cookiecutter.docker_hub_image_name }}
{% else %}
FROM python:3.9
{% endif %}

RUN apt-get update && apt-get install -y \
  git \

COPY ./requirements.txt /requirements.txt
RUN pip install -r /requirements.txt


WORKDIR /