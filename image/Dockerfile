# syntax=docker/dockerfile:1.4

FROM phusion/passenger-full:1.0.1

MAINTAINER Phusion <info@phusion.nl>

ENV HOME /root

# Explicitly copy the install script
ADD install_image.sh /pd_build/install_image.sh

# Ensure the script is executable
RUN chmod +x /pd_build/install_image.sh

# Run the script using nice
RUN ls -la /pd_build && cat /pd_build/install_image.sh

CMD ["/sbin/my_init"]
EXPOSE 80 443

