FROM agrigorev/zoomcamp-model:3.8.12-slim

RUN pip install pipenv

WORKDIR /app

COPY . /app

RUN pip install gunicorn

RUN pipenv install --system --deploy


EXPOSE 9696
ENTRYPOINT ["gunicorn",  "--bind=0.0.0.0:9696", "predict:app"]