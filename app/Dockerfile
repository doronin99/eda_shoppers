FROM python:3.10-slim-buster

RUN pip install explainerdashboard
RUN pip install "pandas<2.0.0"

COPY dashboard.yaml ./
COPY app.py ./
COPY explainer.joblib ./

EXPOSE 5678
CMD ["python", "./app.py"]