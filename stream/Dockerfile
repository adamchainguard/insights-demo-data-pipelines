FROM gradle:latest AS build
WORKDIR /src
COPY build.gradle .
RUN gradle --no-daemon tasks

FROM amazoncorretto:21
WORKDIR /app
CMD ["java", "-version"]
