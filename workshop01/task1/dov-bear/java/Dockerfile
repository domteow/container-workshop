FROM java:17

WORKDIR /app

COPY .mvn .mvn
COPY src src

COPY pom.xml .

RUN mvnw

ENV PORT = 5000

ENV INSTANCE_NAME = "task1_app"

ENV INSTANCE_HASH = ""

EXPOSE ${PORT}

