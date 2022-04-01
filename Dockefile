FROM ubuntu
MAINTAINER SaileshBoguma <bogumasailesh@gmail.com>
RUN apt-get update
RUN apt-get install -y default-jdk
RUN mkdir /opt/tomcat
WORKDIR /opt/tomcat
ADD https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.60/bin/apache-tomcat-9.0.60.tar.gz /opt/tomcat
RUN tar -xvzf apache-tomcat-9.0.60.tar.gz
RUN mv apache-tomcat-9.0.60/* /opt/tomcat
EXPOSE 8080
CMD ["/opt/tomcat/bin/catalina.sh", "run"]
COPY ./*.war /opt/tomcat/webapps

