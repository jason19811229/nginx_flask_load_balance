#
# Nginx Dockerfile
#

# Pull base image.
FROM ubuntu:18.04

# Install Nginx.
RUN apt-get update && \
  apt-get install -y nginx && \
  rm -rf /var/lib/apt/lists/* 


# Define mountable directories.
VOLUME ["/etc/nginx/sites-enabled", "/etc/nginx/certs", "/etc/nginx/conf.d", "/var/log/nginx", "/var/www/html"]

COPY nginx.conf /etc/nginx/nginx.conf
RUN echo "\ndaemon off;" >> /etc/nginx/nginx.conf
# Define working directory.
WORKDIR /etc/nginx

# Define default command.
CMD ["nginx"]

# Expose ports.
EXPOSE 80
EXPOSE 443
