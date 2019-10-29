FROM ubuntu:16.04

RUN  apt-get update  && \
	apt-get install -y git rtmpdump wget ffmpeg python3 python-dev python3-dev python3-setuptools \
    python3-crypto python3-requests python3-lxml \
    php-cli php-curl php-xml php-bcmath \
	build-essential -y && \
	git clone https://github.com/aajanki/yle-dl.git 
WORKDIR yle-dl
RUN python3 setup.py install --user 

ENTRYPOINT ["/root/.local/bin/yle-dl"]

# Command used to build an image from this Dockerifile: sudo docker build -t yle .
# Command to execute yle-dl within a container: sudo docker run -it yle  --showtitle http://yle.fi/aihe/artikkeli/2010/10/28/studio-julmahuvi-roudasta-rospuuttoon
#  Studio Julmahuvi : Roudasta rospuuttoon
#  "Min menen avantoon!"
