# Use a lightweight Python base image
FROM python:3.9-slim

# Set environment variables
ENV HOST=0.0.0.0
ENV PORT=9005
ENV DEBIAN_FRONTEND=noninteractive

# Install system dependencies
RUN apt-get update && apt-get install -y \
    git \
    nodejs \
    npm \
    firefox-esr \
    wget \
    && rm -rf /var/lib/apt/lists/*

# Clone the Social Analyzer repository
WORKDIR /app
RUN git clone https://github.com/qeeqbox/social-analyzer.git .

# Install Python dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Install Node.js dependencies
RUN npm install

# Create a non-root user for security (and HF Spaces compatibility)
RUN useradd -m -u 1000 user
RUN chown -R user:user /app
USER user

# Expose the port
EXPOSE 9005

# Start the application using npm start (which runs the web server)
CMD ["npm", "start"]
