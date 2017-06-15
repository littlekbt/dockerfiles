FROM node:6.9.1
MAINTAINER littlekbt

RUN apt-get update
RUN apt-get install -y vim
# emulator
RUN npm install -g @google-cloud/functions-emulator
# gcloud
RUN apt-get install -y lsb-release
RUN apt-get install -y apt-transport-https

ENV CLOUD_SDK_REPO "cloud-sdk-trusty"
RUN echo "deb https://packages.cloud.google.com/apt $CLOUD_SDK_REPO main" | tee -a /etc/apt/sources.list.d/google-cloud-sdk.list
RUN curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | apt-key add -

RUN apt-get update && apt-get install -y google-cloud-sdk
