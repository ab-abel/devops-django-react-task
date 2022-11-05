FROM python:3.10-slim
ENV PYTHONUNBUFFERED=1
WORKDIR /api

RUN apt-get update \
    && apt-get -y install libpq-dev gcc \
    && pip install psycopg2

COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt
RUN pip install --upgrade pytz
RUN pip install --upgrade django


COPY . .

# EXPOSE 8000
# CMD ["python","manage.py","runserver", "0.0.0.0:8000"] 
