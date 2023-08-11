FROM python:3.9-buster

WORKDIR /app
COPY . /app

#4China users only

RUN pip config set global.index-url http://mirrors.aliyun.com/pypi/simple
RUN pip config set install.trusted-host mirrors.aliyun.com

RUN pip install --no-cache-dir -r requirements.txt

EXPOSE 1010

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "1010"]
