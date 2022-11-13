# My Base Image 
FROM ubuntu:16.04

# Maintainer
MAINTAINER Amit Vashist 

# Update the Apt Repo.
RUN apt-get update 

# Install Apache Packages 
RUN apt-get install apache2 -y 

# Deploy Custom Web Page 
COPY index.html /var/www/html/

# App Listen on Port.
EXPOSE 80

# Bring the Service UP 
CMD ["/usr/sbin/apache2ctl", "-D" , "FOREGROUND"]
