FROM openjdk:8-jdk-alpine

RUN apk updata && apk add redis

COPY jeecg-module-test-3.5.0.jar /app/jeecg-module-tst-3.5.0.jar

EXPOSE 8080

CMD ["java", "-jar", "/app/jeecg-module-tst-3.5.0.jar", \
     "--spring.datasource.url=jdbc:mysql://jeecg-boot-mysql:3306/jeecg-boot", \
     "--spring.datasource.username=root", \
     "--spring.datasource.password=root", \
     "--spring.redis.host=redis-server", \
     "--spring.redis.port=6379"]
