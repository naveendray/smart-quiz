# Use an official Node.js runtime as the base image
FROM node:14

# Set the working directory within the container
WORKDIR /app

# Install json-server globally
RUN npm install -g json-server

# Copy the db.json file into the container
COPY ./db.json /app/data/db.json

# Expose the port for json-server
EXPOSE 8000

# Start json-server
CMD ["sh", "-c", "npx json-server --watch data/db.json --port 8000 --host 0.0.0.0"]
