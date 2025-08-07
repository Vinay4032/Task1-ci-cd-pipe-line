FROM node:18: Uses Node.js v18 official image as the base.
WORKDIR /app: Sets /app as the working directory inside the container.
*COPY package.json ./**: Copies dependency files.
RUN npm install: Installs project dependencies.
COPY . .: Copies all project files into the container.
EXPOSE 3000: Exposes port 3000 for external access.
CMD ["npm", "start"]: Starts the application using the start script from package.json.
