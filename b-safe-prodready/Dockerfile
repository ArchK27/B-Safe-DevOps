FROM ubuntu:20.04
RUN apt-get update
RUN apt-get -y upgrade
RUN apt-get install -y default-jdk
RUN export PATH=$PATH:$JAVA_HOME/bin
RUN apt-get -y install \
apt-transport-https \
ca-certificates \
curl \
gnupg-agent \
software-properties-common
RUN apt-get install -y maven
RUN apt-get install -y git
RUN git clone https://github.com/ArchK27/B-Safe-DevOps.git
WORKDIR ./ArchanaK
RUN mvn clean install
RUN mvn test
RUN mvn clean package
