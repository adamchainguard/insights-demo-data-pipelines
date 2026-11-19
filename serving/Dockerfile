FROM python:3.13 AS build
WORKDIR /src
COPY . .

FROM python:latest
WORKDIR /srv
CMD ["python", "serve.py"]
