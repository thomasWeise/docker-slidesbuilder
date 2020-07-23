#
# thomasweise/docker-slidesbuilder
#
# This is an image with a Tex Live installation with several
# tools to build slides.
# Source: https://github.com/thomasWeise/docker-slidesbuilder/
# License: GNU GENERAL PUBLIC LICENSE, Version 3, 29 June 2007
# The license applies to the way the image is built, while the
# software components inside the image are under the respective
# licenses chosen by their respective copyright holders.
#
FROM thomasweise/docker-texlive-full
MAINTAINER Thomas Weise <tweise@hfuu.edu.cn>

RUN apt-get clean &&\
    apt-get update &&\
    apt-get autoclean -y &&\
    apt-get autoremove -y &&\
    apt-get update &&\
# install necessary components
    apt-get install -f -y git \
                          wget \
                          xz-utils &&\
# clean up all temporary files
    apt-get clean &&\
    apt-get autoclean -y &&\
    apt-get autoremove -y &&\
    apt-get clean &&\
    rm -rf /tmp/* /var/tmp/* &&\
    rm -rf /var/lib/apt/lists/* &&\
    rm -f /etc/ssh/ssh_host_*
