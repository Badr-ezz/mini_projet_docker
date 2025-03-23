
FROM python:3.8-buster


LABEL maintainer="Anas Slimani <anasslimani039@gmail.com>"
LABEL maintainer="Badr Ezziyati <bziyati11@gmail.com>"

RUN mkdir -p /home/app
WORKDIR /app


RUN apt-get update -y && \
    apt-get install -y python3-dev libsasl2-dev libldap2-dev libssl-dev


COPY requirements.txt .


RUN pip3 install --no-cache-dir -r requirements.txt


COPY student_age.py .


RUN mkdir /data
VOLUME /data


EXPOSE 5000


CMD ["python3", "./student_age.py"]