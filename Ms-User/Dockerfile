FROM adoptopenjdk/openjdk11:x86_64-alpine-jre-11.0.6_10

RUN apk add --no-cache tzdata
ENV TZ='America/Lima'
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

COPY target/*.jar application.jar

CMD [ "java", "-jar", "/application.jar" ]