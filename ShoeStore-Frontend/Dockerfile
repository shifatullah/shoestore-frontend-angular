FROM node:12.15.0
RUN mkdir -p /usr/src/ShoeStore-Frontend
COPY dist/ShoeStore-Frontend /usr/src/ShoeStore-Frontend/dist/ShoeStore-Frontend
COPY ssl /usr/src/ShoeStore-Frontend/ssl
COPY authMiddleware.js /usr/src/ShoeStore-Frontend/
COPY serverdata.json /usr/src/ShoeStore-Frontend/
COPY server.js /usr/src/ShoeStore-Frontend/server.js
COPY deploy-package.json /usr/src/ShoeStore-Frontend/package.json
WORKDIR /usr/src/ShoeStore-Frontend
RUN npm install
EXPOSE 80
CMD ["node", "server.js"]