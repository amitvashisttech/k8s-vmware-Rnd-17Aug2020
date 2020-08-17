# Base Image
FROM ubuntu:16.04

# Owner of the Image
MAINTAINER Amit Vashist <amitvashist7@gmail.com>

# Update Apt Repo. 
RUN apt-get update

# Install Apache Packages
RUN apt-get install -y apache2 

# Bring up the Service
CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
