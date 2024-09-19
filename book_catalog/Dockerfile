# Use an official Python runtime as a parent image
FROM python:3.9-slim

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Make port 5000 available to the world outside this container
EXPOSE 5000

# Define environment variable
ENV NAME BookCatalog

# Define environment variable with the provided database URL
ENV DATABASE_URL postgresql://bookdb_lrqd_user:6614odHb7IpbXshtNjdc4weT8B4pgtk6@dpg-crcpujrv2p9s73ckop9g-a.oregon-postgres.render.com/bookdb_lrqd

# Run app.py when the container launches
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "3000"]
