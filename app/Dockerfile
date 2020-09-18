# set base image (host OS)
# FROM thetwintproject/twint:2.1.9-slim
FROM python:3.8-slim

# set the working directory in the container
WORKDIR /code

# copy the dependencies file to the working directory
COPY requirements.txt .

# install dependencies
RUN pip install -r requirements.txt

# copy the content of the local src directory to the working directory
COPY src/ .

# command to run on container start
#CMD [ "python", "./server.py" ]

# comando que evita que el contenedor se pare
CMD [ "tail", "-f", "/dev/null" ]

# expose port 5000
EXPOSE 5000
