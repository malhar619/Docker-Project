1) Clone the Repository.
2) Build the app image:
   i) in the directory same as "pacakge.json" create file named "Dockerfile".
   ii) add the following content to the "Dockerfile":
      FROM node:18-alpine
      WORKDIR /app
      COPY . .
      RUN yarn install --production
      CMD ["node", "src/index.js"]
      EXPOSE 3000
   iii) Build the image using the following commands: "docker build -t folder_name".
3) Start an app container:
   i) Run your container using the docker run command and specify the name of the image you just created:
      'docker run -dp 127.0.0.1:3000:3000 getting-started".
   
   
   
