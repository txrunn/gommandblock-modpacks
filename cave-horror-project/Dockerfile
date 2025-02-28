FROM ghcr.io/graalvm/graalvm-ce:ol8-java17-22.3.3

# Set working directory
WORKDIR /minecraft

# Copy all server files
COPY . /minecraft

# Ensure the eula.txt is accepted
RUN echo "eula=true" > eula.txt

# Make the run.sh script executable
RUN chmod +x run.sh

# Expose Minecraft server port
EXPOSE 25565

# Expose CHP Voice Chat
EXPOSE 25564

# Set the default command to run the server
ENTRYPOINT ["sh", "-c", "./run.sh"]
