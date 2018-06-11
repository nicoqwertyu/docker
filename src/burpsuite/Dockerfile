FROM debian:stretch

EXPOSE 8080

WORKDIR /root/

ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update
RUN apt-get -y install dialog wget default-jre
RUN apt-get clean

RUN wget "https://portswigger.net/burp/releases/download?product=community&version=1.7.33&type=jar" -O burpsuite.jar

RUN mkdir -p /root/.java/.userPrefs/burp/
COPY prefs.xml /root/.java/.userPrefs/burp/

ENTRYPOINT ["java", "-jar", "burpsuite.jar"]

