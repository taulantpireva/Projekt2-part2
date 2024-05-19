# Use the official OpenJDK image from the Docker Hub
FROM openjdk:21-jdk-slim

# Set the working directory in the container
WORKDIR /usr/src/app

# Copy the project files
COPY . .

# Package the application, skipping tests
RUN ./mvnw -Dmaven.test.skip=true package

# Make port 8080 available to the world outside this container
EXPOSE 8080

# Define the command to run the application
CMD ["java", "-jar", "/usr/src/app/target/playground-0.0.1-SNAPSHOT.jar"]
