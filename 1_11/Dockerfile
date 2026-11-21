FROM amazoncorretto:8

WORKDIR /usr/src/app

COPY . .

RUN sed -i 's/\r$//' ./mvnw && chmod +x ./mvnw && ./mvnw package

CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]