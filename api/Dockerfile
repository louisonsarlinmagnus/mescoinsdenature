# syntax=docker/dockerfile:1
FROM python:3
LABEL maintainer "Louison SARLIN--MAGNUS <louisonsm.pro@gmail.com>"

ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED 1

#Move the requirement from the directory into the container
COPY ./requirements.txt /requirements.txt

#Installing the requirements detailled in the file located in the container
RUN pip install -r requirements.txt

#Switching to this repo
WORKDIR /app
#Copying our local repo app to the one in the container
COPY . .

#Creating a user to run the application
RUN useradd django
#Swithcing to that user
USER django

#Exposing the port to acess the app
EXPOSE 2804
