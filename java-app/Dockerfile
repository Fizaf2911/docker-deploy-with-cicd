FROM amazoncorretto:17

WORKDIR /app

COPY App.java .

RUN javac App.java

RUN yum install -y shadow-utils

RUN useradd -m appuser

RUN chown -R appuser:appuser /app

USER appuser

EXPOSE 8080

CMD ["java", "App"]
