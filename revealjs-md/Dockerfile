FROM node

MAINTAINER Guilherme Dantas <gamsd@gamsd.com>

RUN wget https://github.com/hakimel/reveal.js/archive/3.2.0.tar.gz
RUN tar xzf 3.2.0.tar.gz
RUN mv /reveal.js-3.2.0 /revealjs

RUN mkdir -p /revealjs/md/images

WORKDIR /revealjs

RUN npm install -g grunt-cli
RUN npm install
RUN sed -i Gruntfile.js -e 's/port: port,/port: port, hostname: "",/'

ADD index.html /revealjs/

ONBUILD ADD slides.md /revealjs/md/
ONBUILD ADD images /revealjs/md/images

EXPOSE 8000
VOLUME ["/revealjs/md/"]
CMD ["grunt", "serve"]
