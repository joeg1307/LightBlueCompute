FROM openjdk:8-jre-alpine
VOLUME /tmp
ADD app.jar app.jar
RUN apk --no-cache update && apk add jq bash bc
RUN bash -c 'touch /app.jar'

COPY startup.sh startup.sh
EXPOSE 8080
ENTRYPOINT ["./startup.sh"]
