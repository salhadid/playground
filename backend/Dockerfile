FROM python:3.10-bullseye
RUN python -m pip install --upgrade pip
WORKDIR /app

# Copy the top-level files in your service's directory
COPY requirements.txt requirements.txt
COPY main.py main.py

# Copy all of the subdirectories in your service's directory

RUN python -m pip install -r requirements.txt

# !! PORT env var needs to match with exposed port in caprover dashboard
CMD uvicorn backend.main:app --host 0.0.0.0 --port 8000

# COPY migrations migrations

# CMD python -m migrations up && uvicorn main:app --host 0.0.0.0 --port 8000
