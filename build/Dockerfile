FROM ubuntu:20.04
RUN apt-get update
RUN apt-get install default-jdk -y
RUN apt-get install git -y
RUN apt-get install maven -y
WORKDIR /home/dz12/
RUN git clone https://github.com/shephertz/App42PaaS-Java-MySQL-Sample.git
WORKDIR /home/dz12/App42PaaS-Java-MySQL-Sample/

WORKDIR home/dz12/App42PaaS-Java-MySQL-Sample/WebContent
RUN echo "app42.paas.db.username = paasdb_user" >> Config.properties
RUN echo "app42.paas.db.port = 3306" >> Config.properties
RUN echo "app42.paas.db.password = pass123" >> Config.properties
RUN echo "app42.paas.db.ip = db" >> Config.properties
RUN echo "app42.paas.db.name = paasdb" >> Config.properties

RUN mvn package