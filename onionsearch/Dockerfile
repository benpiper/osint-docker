FROM python:3.8-slim-buster

ENV PYTHONDONTWRITEBYTECODE=1

ENV PYTHONUNBUFFERED=1

RUN apt-get update \
&& apt-get install -y --no-install-recommends git \
&& apt-get purge -y --auto-remove \
&& rm -rf /var/lib/apt/lists/*
RUN git clone https://github.com/megadose/onionsearch.git \
&& cd onionsearch/ \
&& python3 setup.py install

WORKDIR /bin

ENTRYPOINT [ "onionsearch" ]
CMD ["onionsearch", "--help"]
