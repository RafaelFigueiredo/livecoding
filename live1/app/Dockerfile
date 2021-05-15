FROM python:3-buster


WORKDIR /app

ADD requirements.txt .
RUN pip install -r requirements.txt

RUN groupadd -r appuser && useradd --no-log-init -r -g appuser appuser
USER appuser

ADD main.py .


ENTRYPOINT ["uvicorn","main:app","--host", "0.0.0.0","--port","5000"]

