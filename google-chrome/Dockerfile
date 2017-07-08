FROM debian:latest

RUN sh -c 'echo "deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list'
RUN apt-get update;  apt-get install -y wget gnupg
RUN wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add -
RUN apt-get update
RUN apt-get install -y google-chrome-stable pulseaudio

RUN useradd -r -u 1234 -g 100 -G audio,video chrome \
    && mkdir -p /home/chrome/Downloads
USER chrome

CMD [ "google-chrome" ]
