# Use the official Rust image as the parent image
FROM rust:1.58

# Set the working directory to /app
WORKDIR /chat-app

# Copy the Cargo.toml and Cargo.lock files into the container
COPY Cargo.toml Cargo.lock ./

# Copy the source code into the container
COPY src/ ./src/

# Build the Rust application
RUN cargo build --release

# Expose port 8000
EXPOSE 8000

# Set the command to run when the container starts
CMD ["./target/release/chat-app"]
