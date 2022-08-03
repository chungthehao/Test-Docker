# Use this parent image to build my own image (as the 1st layer)
FROM node:17-alpine

# Specify the working directory in the image, so '.' means '/app' in the image
WORKDIR /app

# Copy all data from current folder (my actual computer) to '/app' in the image [ignore some stuff in .dockerignore]
COPY . .

# Install all the dependencies as the image is being built
RUN npm install

# Expose the port that I want, in this case my node app listening in port 4000
EXPOSE 4000

# Run this cmd after a container built from this image
CMD [ "node", "app.js" ]