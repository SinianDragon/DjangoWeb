FROM python:3.8
MAINTAINER WGR
ENV PYTHONUNBUFFERED 1

RUN apt-get update
RUN apt-get install -y apt-utils libjpeg-dev python3-pip
RUN pip install --upgrade pip
RUN pip install --upgrade setuptools

WORKDIR /web
COPY . /web
# RUN python manage.py collectstatic --noinput
RUN pip install -r requirements.txt


EXPOSE 8000

# Running the Django server
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
