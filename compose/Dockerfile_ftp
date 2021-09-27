FROM ubuntu:18.04

# Install software 
RUN apt-get update
RUN apt-get install -y git

# Clone the conf files into the docker container
RUN git clone https://github.com/YevheniiOnishchenko/docker-alpine-ftp-server.git

RUN apt install -y vsftpd

RUN mkdir /etc/vsftpd


RUN cp docker-alpine-ftp-server/start_vsftpd.sh /bin/start_vsftpd.sh

RUN cp docker-alpine-ftp-server/vsftpd.conf /etc/vsftpd/vsftpd.conf

ENTRYPOINT ["/bin/start_vsftpd.sh"]
