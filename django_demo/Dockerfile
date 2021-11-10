FROM python:3.7
ENV PYTHONUNBUFFERED 1
RUN mkdir /code
WORKDIR /code
COPY . /code

RUN chmod -R 777 /code
RUN pip install --upgrade pip 

RUN pip install -r requirements.txt
EXPOSE 8000
CMD python manage.py makemigrations && python manage.py migrate && python manage.py runserver 0.0.0.0:8000