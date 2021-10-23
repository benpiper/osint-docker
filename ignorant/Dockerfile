FROM python:3.8-slim-buster

ENV PYTHONDONTWRITEBYTECODE=1

ENV PYTHONUNBUFFERED=1

RUN apt-get update \
&& apt-get install -y --no-install-recommends git \
&& apt-get purge -y --auto-remove \
&& rm -rf /var/lib/apt/lists/*
RUN git clone https://github.com/megadose/ignorant.git \
&& cd ignorant/ \
&& python3 setup.py install

WORKDIR /bin

ENTRYPOINT [ "ignorant" ]
CMD ["ignorant"]
