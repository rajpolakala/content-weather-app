# content-weather-app
Travis Weather App

FROM node
LABEL org.label-schema.version=v1.1
ENV NODE_ENV="production"
ENV PORT 3001

RUN mkdir -p /var/node
ADD src/ /var/node/
WORKDIR /var/node
RUN npm install
EXPOSE $PORT
CMD ./bin/www
