FROM python:3.7
ENV PYTHONUNBUFFERED 1
ENV C_FORCE_ROOT true
COPY . /code
WORKDIR /code
RUN chmod -R 777 /code
RUN pip install -r requirements.txt
EXPOSE 8080
CMD python manage.py makemigrations && python manage.py migrate && python manage.py runserver 0.0.0.0:8000