FROM debian
RUN apt-get update && apt-get install -y --no-install-recommends apt-utils
RUN apt-get install -y wget bzip2 && apt-get clean
RUN wget https://files.teamspeak-services.com/releases/server/3.8.0/teamspeak3-server_linux_amd64-3.8.0.tar.bz2 && tar -xjf teamspeak3-server_linux_amd64-3.8.0.tar.bz2
RUN rm -rf teamspeak3-server_linux_amd64-3.8.0.tar.bz2
RUN mkdir /home/teamspeak && mv teamspeak3-server_linux_amd64/* /home/teamspeak/. && rm -rf teamspeak3-server_linux_amd64
RUN touch /home/teamspeak/.ts3server_license_accepted

EXPOSE 30033/tcp
EXPOSE 10011/tcp
EXPOSE 9987/udp

ENTRYPOINT ["/home/teamspeak/ts3server_minimal_runscript.sh", "start"]
# to build docker build -t ex01 .
# to run docker run --rm -p 9987:9987/udp -p 10011:10011 -p 30033:30033 --env TS3SERVER_LICENSE=accept ex01
