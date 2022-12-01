FROM python:3.11-slim

RUN --mount=type=cache,target=/var/lib/apt/lists \
    --mount=type=cache,target=/var/cache,sharing=locked \
    apt-get update \
    && apt-get upgrade --yes

COPY requirements.txt /app/
RUN --mount=type=cache,target=/root/.cache \
    pip install --disable-pip-version-check --requirement=/app/requirements.txt

COPY *.py /app/

CMD ["python", "/app/updater.py"]
