FROM python:3.9-slim

WORKDIR /app

COPY requirements.txt .
RUN pip install -r requirements.txt

COPY . .

RUN python -c "from app import init_db; init_db()"

EXPOSE 8080

CMD ["python", "app.py"]