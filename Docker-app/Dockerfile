FROM openjdk:11 AS build_image
RUN apt update && apt install maven -y
RUN git clone https://github.com/Ashsatsan/eks-integration.git
RUN cd vprofile-project && mvn install

FROM tomcat:9-jre11
RUN rm -rf /usr/local/tomcat/webapps/*
COPY --from=build_image vprofile-project/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war

EXPOSE 8080
CMD ["catalina.sh", "run"]
