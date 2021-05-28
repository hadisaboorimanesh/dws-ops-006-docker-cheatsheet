From python:slim

LABEL maintainer="hadi saboori"
WORKDIR /opt/app

expose 8080

ENV SKOB_AUTHZ_BIND_ADDRESS=0.0.0.0
ENV SKOB_AUTHZ_NUM_WORKER=4

COPY requirments.txt .
RUN pip install -r requirments.txt

COPY . .

RUN useradd -M -d /opt/app authz
USER authz

CMD ./start
