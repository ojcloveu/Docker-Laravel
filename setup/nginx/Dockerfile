# Use the official Nginx image as the base image
FROM nginx:latest

USER nginx
# Copy your custom Nginx configuration file to the container
# COPY nginx.conf /etc/nginx/conf.d/default.conf




# Expose port 80 (the default Nginx port)
EXPOSE 80

# Start Nginx
CMD ["nginx", "-g", "daemon off;"]
