FROM python:3.10-slim-buster

WORKDIR /backend-flask

COPY requirements.txt requirements.txt

# RUN: is runned to create a layer in the image ## Here packages in the requirement.txt
# are installed, creating a layer in the docker image
RUN pip3 install -r requirements.txt

COPY . .

ENV FLASK_ENV=development

EXPOSE ${PORT}
# CMD (Command).: command to run in container
# python3 -m flask run --host=0.0.0.0 --port=4567
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]