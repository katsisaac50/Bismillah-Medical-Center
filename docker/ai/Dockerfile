FROM tensorflow/tensorflow:latest-gpu

WORKDIR /app
COPY ./ai-models /app/models
COPY ./server/services/ai /app/services

RUN apt-get update && \
    apt-get install -y python3 python3-pip && \
    pip3 install tensorflowjs

CMD ["node", "/app/services/ai-worker.js"]
