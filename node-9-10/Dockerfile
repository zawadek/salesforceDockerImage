FROM node:9.10.0-alpine

# install git ca-certificates openssl openssh
RUN apk add --update --no-cache bash git openssh ca-certificates openssl jq

# install latest sfdx from npm
RUN npm install sfdx-cli --global && \
    sfdx --version && \
    sfdx plugins --core

# revert to low privilege user
USER node

CMD [ "bin/bash" ]