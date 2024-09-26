FROM python:3.9

#set the working directory
WORKDIR /usr/src/app

#copy dependency files to the working directory
COPY requirements.txt ./

#Installing dependencies
RUN pip install --no-cache -r requirements.txt
RUN pip install fastapi-cors

#copy the contents of local directory to the working directory
COPY .  .

#CMD ["fastapi", "run", "api/main.py", "80"]
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]