# Build container from this image
FROM python:3.10-slim-buster

# Inside container
# create a new folder and change to this directory
WORKDIR /backend-flask

# Copy the file from Outside Container to Inside Container
# this contains the libraries want to install to run the app
COPY requirements.txt requirements.txt

# Inside Container
# Install the python libraries used for the app
# RUN is a Layer part of the setup of the container
RUN pip3 install -r requirements.txt

# Outside Container to Inside Container
# . means everything in the current directory
# first period . -  /backend-flask (outside container)
# second period . /backend-flask (inside container)
COPY . .


# Set Envirionment Variables (Env Vars)
# Inside Container and will remain set when the container is running
ENV FLASK_ENV=development


EXPOSE ${PORT}

# CMD (Command)
# python3 -m flask run --host=0.0.0.0 --port=4567 ""
# CMD is a command to execute after the container is ready
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]