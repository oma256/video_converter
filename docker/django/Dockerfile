FROM python:3.7
MAINTAINER  Dulatov Omurbek <oma.dulatov@gmail.com>

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

WORKDIR /app

RUN apt-get update && apt-get install -y ffmpeg

COPY Pipfile Pipfile.lock ./
RUN pip install --upgrade pip && pip install pipenv
RUN pipenv install --system

COPY . .

EXPOSE 8000