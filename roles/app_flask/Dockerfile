FROM ubuntu:latest
MAINTAINER Your Name "zuuuuper-meh@crash-test.fr"
RUN apt update && apt install python3-pip

# We copy just the requirements.txt first to leverage Docker cache
RUN mkdir -p app
COPY ../../requirements.txt /app/requirements.txt
WORKDIR /app
RUN pip install -r requirements.txt
COPY . .
ENTRYPOINT ["python3"]
CMD ["../../app/app.py"]
