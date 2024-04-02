FROM python:3.8

WORKDIR /app

COPY requirements.txt /app
COPY pythonProject /app/pythonProject

RUN apt-get update && \
    pip install -r requirements.txt && \
    chmod -R 777 /app && \
    chmod -R 777 /app/pythonProject

WORKDIR /app/pythonProject

EXPOSE 8000

ENTRYPOINT ["python3"]
CMD ["app.py", "runserver", "0.0.0.0:8000"]
