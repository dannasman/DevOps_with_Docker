FROM ubuntu:18.04

EXPOSE 5000

WORKDIR /usr/src/app

RUN apt-get update && apt-get install -y curl

RUN curl -sL https://deb.nodesource.com/setup_14.x | bash -
RUN apt install -y nodejs

COPY . .

ENV REACT_APP_BACKEND_URL=http://localhost:3001

RUN npm install && npm run build && npm install -g serve

CMD ["serve", "-s", "-l", "5000", "build"]
