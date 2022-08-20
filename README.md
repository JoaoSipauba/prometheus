# Creating volume to persist data
docker volume create prometheus_data

# Building the image from dockerfile
docker build -t my-prometheus .

# Bunning container with specific params
docker run -d --name prometheus -v prometheus_data:/prometheus -p 9090:9090 my-prometheus