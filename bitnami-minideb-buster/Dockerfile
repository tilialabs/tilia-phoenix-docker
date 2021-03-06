# Tilia Labs Inc.
# Copyright (c) 2012-*, All Rights Reserved
#
# Phoenix Minideb Buster Docker image
#
# Building and running an image:
#
# 1. Download Phoenix Auto Debian package (deb) from downloads.tilialabs.com
#
# 2. Build docker image in folder containing the package downloaded in step #1
#
#    docker build -t IMAGE_NAME --build-arg package=PACKAGE_FILE .
#
#    IMAGE_NAME   is the name of the image you want, e.g. tilia-phoenix:8.0
#    PACKAGE_FILE is the filename of the Deb package downloaded in step #1
#
#    NOTE: If this Dockerfile is in another folder you can reference it using
#          -f /path/to/this/Dockerfile
#
# 3. Run a container using this image
#
#    docker run -p 8080:8022 IMAGE_NAME -p 8022 -u USERNAME -pw PASSWORD
#
#    IMAGE_NAME is the name you used in step #2
#    USERNAME   is the name of a user in Tilia Cloud that can consume a valid
#               Phoenix license that includes automation
#    PASSWORD   is password of the Tilia Cloud user
#
#    NOTE: The first "-p" argument before IMAGE_NAME maps the TCP port inside
#          the container (8022 in example above) to the host port (8080), while
#          the second "-p" argument is passed into Phoenix to specify the port
#          it uses inside the container.  The two container-side ports must
#          match but can be mapped to a different host port.

# Using Bitnami Minideb Buster as base image
FROM bitnami/minideb:buster

# Set working directory to /usr/local/src to copy local installer over
WORKDIR /usr/local/src

# Install dbus
RUN install_packages dbus

# Build argument of Phoenix Auto debian package file name
ARG package=PhoenixAuto.deb

# Copy debian package on host to docker image
COPY $package .

# Run Phoenix Installer in the docker image
RUN dpkg -i $package

# Now Phoenix is installed set working directory to installed location
WORKDIR /opt/tilialabs/tilia-phoenix-auto

# Set user to tilialabs which was created in debian package install step
USER tilialabs

# Entrypoint to launch Phoenix with no default arguments
ENTRYPOINT ["./tilia-phoenix-auto"]
