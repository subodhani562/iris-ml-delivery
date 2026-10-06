FROM python:3.12-slim
WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir --default-timeout=20 --retries 10 -r requirements.txt

COPY train.py app.py ./
RUN python train.py

EXPOSE 5000
CMD ["python", "app.py"]
(Get-Content Dockerfile -Raw) -replace "`r`n","`n" | Set-Content -NoNewline Dockerfile