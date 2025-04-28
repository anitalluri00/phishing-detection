FROM amazonlinux:2

RUN yum update -y && \
    yum install -y python3 python3-pip && \
    yum install -y gcc gcc-c++ make

COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt

WORKDIR /app

COPY . .

EXPOSE 5000

CMD ["python3", "app.py"]
