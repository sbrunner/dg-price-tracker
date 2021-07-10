FROM python:3.7-slim

COPY requirements.txt /app/
RUN pip install --no-cache-dir -r /app/requirements.txt

COPY *.py /app/

CMD ["python", "/app/updater.py"]
