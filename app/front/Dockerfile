# Use nginx runtime as a parent image
FROM nginx:latest

# Set the working directory in the container
WORKDIR /usr/share/nginx/html

# Copy the current directory contents into the container at /app
COPY . .

RUN chmod +x /usr/share/nginx/html/entrypoint.sh

# Define environment variable
ENV WS_BACK_URL=http://back_app:5000

# Run nginx when the container launches
ENTRYPOINT [ "/usr/share/nginx/html/entrypoint.sh" ]