FROM python:3.11-sliim

#installing dependencies
RUN pip install pandas numpy matplotlib fastapi uvicorn

#create folder in container
WORKDIR /app
#copying sandbox_server file into app folder
COPY sandbox_server.py /app

#uvicorn to access sandbox_server application ('app' being FastAPI application instance)
#0.0.0.0 -> any IP address
#listen on port 8000
CMD ["uvicorn", "sandbox_server:app", "--host", "0.0.0.0", "--port", "8000"]