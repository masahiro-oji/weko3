FROM python:3.12

ENV PYTHONUNBUFFERED True
ENV APP_HOME /app
WORKDIR $APP_HOME

RUN apt-get update && apt-get install -y git
RUN git clone https://github.com/RCOSDP/coar-notify-inbox.git $APP_HOME

RUN pip install --upgrade pip
RUN pip install --no-cache-dir -r requirements.txt --prefer-binary

CMD ["uvicorn", "app:app", "--host", "0.0.0.0", "--port", "8080"]
