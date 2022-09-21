FROM jenkins/jenkins:lts-alpine
USER root
RUN apk add --no-cache python3 && \
 python3 -m ensurepip && \
 pip3 install --upgrade pip setuptools && \
 if [ ! -e /usr/bin/pip ]; then ln -s pip3 /usr/bin/pip ; fi && \
 if [[ ! -e /usr/bin/python ]]; then ln -sf /usr/bin/python3 /usr/bin/python; fi && \
 rm -r /root/.cache && \
 pip install ansible --upgrade

RUN apk add pkgconf
RUN apk add build-base
RUN apk add python3-dev

USER jenkins