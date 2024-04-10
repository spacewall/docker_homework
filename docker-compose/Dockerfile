FROM python:latest

WORKDIR /usr/src/project
COPY requirements.txt ./
RUN pip install -r requirements.txt
COPY . .

EXPOSE 8080

RUN python manage.py migrate
CMD ["gunicorn", "stocks_products.wsgi", "-b", "0.0.0.0:8080"]
