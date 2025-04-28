# Use Amazon Linux 2 base
FROM amazonlinux:2

# Update and install necessary tools
RUN yum update -y && \
    yum install -y python3 python3-pip gcc gcc-c++ make

# Install Flask directly
RUN pip3 install flask

# Set the working directory
WORKDIR /app

# Copy all files into container
COPY . .

# Set environment variable for Flask
ENV FLASK_APP=app.py

# Expose port 5000
EXPOSE 5000

# Command to run Flask app
CMD ["flask", "run", "--host=0.0.0.0", "--port=5000"]
