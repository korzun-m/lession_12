FROM openjdk:7-jdk
RUN apt-get update
RUN apt-get -y install maven git
RUN git clone https://github.com/shephertz/App42PaaS-Java-MySQL-Sample.git  /tmp/App42PaaS-Java-MySQL-Sample
ADD Config.properties /tmp/App42PaaS-Java-MySQL-Sample/WebContent/Config.properties
RUN mvn -f /tmp/App42PaaS-Java-MySQL-Sample/pom.xml package
RUN mkdir /apps/root
RUN mkdir /apps/webapps
RUN cp -r /tmp/App42PaaS-Java-MySQL-Sample/WebContent/* /apps/toot
RUN cp /tmp/App42PaaS-Java-MySQL-Sample/target/*.war /apps/webapps