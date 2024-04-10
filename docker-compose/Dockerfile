FROM python:latest

WORKDIR /app
COPY requirements.txt ./
RUN pip install --upgrade pip && pip install gunicorn && pip install -r requirements.txt
COPY . .

EXPOSE 8000

# CMD ["gunicorn", "stocks_products.wsgi", "-w", "4", "-t", "600", "-b", "0.0.0.0:8000"]
CMD [ "python", "manage.py", "migrate" ]
