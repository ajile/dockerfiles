FROM ajile/dockerfiles:google-chrome

# Install utilities
RUN apt-get update --fix-missing && \
    apt-get -y upgrade && \
    apt-get install -y curl git apt-transport-https

# Install Yarn
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - && \
    echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list && \
    apt-get update && apt-get install -y yarn

# Install global Node dependencies
RUN npm i --silent -g bower && \
    npm i --silent -g node-sass@4.4.0 && \
    npm i --silent -g ember-cli@2.9.0
