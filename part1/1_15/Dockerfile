FROM alpine:3.9.4
WORKDIR /usr/src/app

RUN apk add bash
RUN apk add git
RUN apk add nodejs-npm

RUN git clone https://github.com/Gomabaen/simple_app.git
WORKDIR /usr/src/app/simple_app
RUN npm install -g @angular/cli
RUN npm install
#ENTRYPOINT ["npm", "start"]
