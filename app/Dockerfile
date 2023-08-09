FROM python:3.10-slim-buster

RUN pip install explainerdashboard

COPY dashboard.yaml ./
COPY app.py ./

EXPOSE 5678
CMD ["python", "./app.py"]