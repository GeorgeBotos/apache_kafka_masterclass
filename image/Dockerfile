FROM eclipse-temurin:17-jre-focal

ADD https://archive.apache.org/dist/kafka/3.3.2/kafka_2.12-3.3.2.tgz kafka.tgz

RUN tar -xvzf kafka.tgz

RUN rm kafka.tgz

RUN mv /kafka_2.12-3.3.2 /kafka

ENV PATH=${PATH}:/kafka/bin

WORKDIR learning

ADD runner.sh runner.sh

CMD [ "sh", "runner.sh" ]