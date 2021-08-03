FROM python:3.9
EXPOSE 8000

ENV mode="development"
COPY /app /app
WORKDIR /app

RUN pip install -r requirements.txt \
    && django-admin startproject mysite . \
    && python manage.py makemigrations \
    && python manage.py migrate

CMD python manage.py runserver 0.0.0.0:8000