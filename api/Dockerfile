FROM python:3.9

WORKDIR /app

COPY requirements.txt /app/requirements.txt

RUN pip install -r /app/requirements.txt && mkdir api

COPY . /app/api/

#CMD ["fastapi", "run", "api/main.py", "80"]
CMD ["uvicorn", "api.main:app", "--host", "0.0.0.0", "--port", "80"]