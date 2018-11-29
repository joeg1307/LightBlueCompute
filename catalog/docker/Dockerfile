FROM openjdk:8-jre-alpine
VOLUME /tmp
ADD app.jar app.jar
RUN bash -c 'touch /app.jar'

# Install prereq
RUN apk --no-cache update && apk add jq bash bc

COPY startup.sh startup.sh
EXPOSE 8081
ENTRYPOINT ["./startup.sh"]
