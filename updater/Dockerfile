FROM python:3.10.4-slim

RUN --mount=type=cache,target=/var/lib/apt/lists \
    --mount=type=cache,target=/var/cache,sharing=locked \
    apt-get update \
    && apt-get upgrade --yes

COPY requirements.txt /app/
RUN pip install --no-cache-dir -r /app/requirements.txt

COPY *.py /app/

CMD ["python", "/app/updater.py"]
