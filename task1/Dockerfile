# Use the latest Ubuntu image
FROM ubuntu:latest

# Uptade the APT package manager
RUN apt-get update && apt-get upgrade -y

# Install Python 3 and pip 3
RUN apt-get install -y python3 python3-pip

# Fix the EXTERNALLY-MANAGED error if it occurs
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Pip install flask
RUN pip3 install flask

# Set /app as the working dr
WORKDIR /app

# Copy the api.py file to /app directory in the container
COPY ./api.py /app/api.py

# Expose port 5252
EXPOSE 5252

# Run app 
CMD ["python3", "api.py"]