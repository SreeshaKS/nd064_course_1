FROM python:3

LABEL maintainer="Sreesha S Kuruvadi"

COPY ./techtrends /app

WORKDIR /app

#install packages defined in the requirements.txt file
RUN pip install -r requirements.txt

#database is initialized with the pre-defined posts in the init_db.py
RUN python ./init_db.py

#expose the application port 7111
ENV PORT 7111
EXPOSE ${PORT}

# command to run on container start
CMD [ "python3", "app.py" ]