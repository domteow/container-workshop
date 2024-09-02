FROM node:22

WORKDIR /app


# copy from local to container (in curr dir)
COPY main.js .
COPY package*.json .

# cos u want these to be in their folders not in /app
COPY public public 
COPY views views

RUN npm ci

ENV PORT=3000

ENV INSTANCE_NAME="task1_app"

ENV INSTANCE_HASH=""

HEALTHCHECK --interval=30s --timeout=30s --start-period=5s --retries=3 \
 CMD curl -s localhost:${PORT}/healthz || exit 1

EXPOSE ${PORT}

ENTRYPOINT node main

