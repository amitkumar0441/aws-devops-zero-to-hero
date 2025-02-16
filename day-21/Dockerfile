FROM python:3.9-slim

# Set the working directory
WORKDIR /app

# Install system dependencies if required
RUN apt-get update && apt-get install -y gcc libpq-dev && rm -rf /var/lib/apt/lists/*

# Copy requirements and install dependencies
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy application code
COPY app.py .

# Expose the required port
EXPOSE 3000

# Start the Flask application
CMD ["python", "app.py"]
