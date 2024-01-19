# Choose base image
FROM ubuntu

# Set working directory
WORKDIR /app

# Copy requirements and source to work directory
COPY requirements.txt /app
COPY devops /app

# Install app dependencies
RUN apt-get update && \
    apt-get install -y python3 python3-pip && \
    pip install -r requirements.txt && \
    cd devops

# Set entry point and cmd (starting commands)
ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]




