From jenkins/jenkins:2.127

USER root
RUN curl -sL https://deb.nodesource.com/setup_8.x | bash -
RUN apt-get update
#Downloading cypress dependencies 
RUN apt-get install -y xvfb libgtk2.0-0 libnotify-dev libgconf-2-4 libnss3 libxss1 libasound2
RUN apt-get install nodejs
RUN npm doctor
# Creating the cache file for cypress
RUN mkdir /root/.cache


#Docker installation

RUN apt-get install -y apt-transport-https ca-certificates curl 
RUN apt-get install -y gnupg2 software-properties-common
RUN curl -fsSL https://download.docker.com/linux/debian/gpg | apt-key add -
RUN add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/debian $(lsb_release -cs) stable"
RUN apt-get update

#WARNING : install a specific version here
RUN apt-get install -y docker-ce

