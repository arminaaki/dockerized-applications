FROM debian:latest

RUN echo deb http://security.debian.org/debian-security wheezy/updates main > /etc/apt/sources.list.d/spotify.list
RUN apt-get update; apt-get install -y gnupg

RUN apt-get install -y libssl1.0.0
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys BBEBDCB318AD50EC6865090613B00F1FD2C19886 \
	&& echo deb http://repository.spotify.com stable non-free > /etc/apt/sources.list.d/spotify.list \
	&& apt-get update \
	&& apt-get install -y \
		spotify-client \
                pulseaudio \
	&& apt-get clean

CMD ["spotify"]
