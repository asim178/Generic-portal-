# Use official Python image
FROM python:3.11-slim

# Set working directory
WORKDIR /app

# Copy and install dependencies
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy project files
COPY . .

# Expose port (your app port)
EXPOSE 8000

# Run the application
CMD ["gunicorn", "project_name.wsgi:application", "--bind", "0.0.0.0:8000"]
