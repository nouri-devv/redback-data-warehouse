# Use the official Python image from the Docker Hub
FROM python:3.9-slim

# Set the working directory in the container
WORKDIR /

# Copy the requirements file into the container
COPY requirements.txt .

# Install the dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application code into the container
COPY . .

# Copy the .env file into the container
COPY dw.env .

# Expose the port the app runs on
EXPOSE 5000

# Command to run the api
CMD ["python", "api.py"]