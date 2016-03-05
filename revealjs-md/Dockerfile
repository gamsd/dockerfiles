FROM parente/revealjs

RUN mkdir -p /revealjs/md/images

ADD index.html /revealjs/

ONBUILD ADD slides.md /revealjs/md/
ONBUILD ADD images /revealjs/md/images
