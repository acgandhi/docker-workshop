# based on slim version of python 3.12 debian image
FROM python:3.12-slim-bookworm

# create working directory
WORKDIR /code

# Environment variables for flask
ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0

# install python dependencies
COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt

# expose port 5000
EXPOSE 5000

# copy rest of code
COPY . .

# default command for container
CMD ["flask", "run"]
