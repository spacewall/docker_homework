FROM python:latest

WORKDIR /usr/src/project
COPY requirements.txt ./
RUN pip install -r requirements.txt
COPY . .

EXPOSE 8000

RUN python manage.py migrate
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]