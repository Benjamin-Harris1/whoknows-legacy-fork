FROM python:3.9-slim

WORKDIR /app

COPY ../backend/requirements.txt .
RUN pip install -r requirements.txt

COPY ../backend .
COPY ../schema.sql ../schema.sql

RUN python -c "from app import init_db; init_db()"

EXPOSE 8080

CMD ["python", "app.py"]