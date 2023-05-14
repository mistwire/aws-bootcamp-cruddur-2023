FROM python:3.10-slim-buster

# Inside container
WORKDIR /backend-flask

# Move file from repo to inside container
COPY requirements.txt requirements.txt

# Inside container run pip3 & install python libraries
RUN pip3 install -r requirements.txt

# Copy all files from /backend-flask in repo to /backend-flask in container
COPY . .

# Set environment variables inside container 
ENV FLASK_ENV=development

# 
EXPOSE ${PORT}

# Inside container run CMD python3 -m flask run --host=0.0.0.0 --port=4567 
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]

# run this after build docker run --rm -p 4567:4567 -it -e FRONTEND_URL='*' -e BACKEND_URL='*' backend-flask
# add /api/activities/home to URL 