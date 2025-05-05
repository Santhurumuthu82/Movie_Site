FROM node:22
WORKDIR /client
COPY . .
RUN npm install 
RUN npm install nodemon
RUN npm install axios
RUN npm install papaparse
RUN npm install  -g serve
CMD ["npm","start"]