# Use the official NGINX image from Docker Hub
FROM nginx:latest

# Remove the default configuration (if needed)
RUN rm -rf /etc/nginx/nginx.conf

# Copy your custom NGINX configuration to the correct location
COPY nginx.conf /etc/nginx/nginx.conf

# Expose the NGINX port
EXPOSE 80

# Start NGINX in the foreground (to prevent container exit)
CMD ["nginx", "-g", "daemon off;"]
