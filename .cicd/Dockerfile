# Need to create a Dockerfile for java based applications
# Dockerfile for Eureka

FROM openjdk:18.0.2.1-jdk
ARG JAR_SOURCE
ENV JAR_SOURCE ${JAR_SOURCE}
ARG JAR_DEST
ENV JAR_DEST ${JAR_DEST}
RUN mkdir -p /opt/product/
WORKDIR /opt/product/
COPY ["${JAR_SOURCE}", "/opt/product/product-service.jar"]
RUN chmod 777 /opt/product/
EXPOSE 8132
CMD ["java", "-jar", "/opt/product/product-service.jar"]
