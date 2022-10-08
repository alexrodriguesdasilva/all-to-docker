#docker build -t alexrodriguesdasilva/example-website-python-flask:1.0.0 .
#docker run -d -p 80:5000 --name example-website-python-flask alexrodriguesdasilva/example-website-python-flask:1.0.0

FROM python:3.8-alpine

LABEL version="1.0.0" \
      description="python/flask containerized application" \
      maintainer="Alex Rodrigues da Silva <alex_horo@hotmail.com>"

WORKDIR /app

COPY ./app .

RUN pip install -r requirements.txt

EXPOSE 5000

CMD ["python","app.py"]