FROM node:7.4.0

# Install utilities
RUN apt-get update --fix-missing && \
    apt-get -y upgrade && \
    apt-get install -y \
    sudo wget

# Install Chrome for Ubuntu
RUN wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add - && \
    sudo sh -c 'echo "deb http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google-chrome.list' && \
    sudo apt-get update && \
    sudo apt-get install -y \
    google-chrome-unstable

# Expose port 9222
EXPOSE 9222
