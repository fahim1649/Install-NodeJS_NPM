# Install-NodeJS_NPM

#!/bin/bash

# Download Node.js LTS 
wget https://nodejs.org/dist/v22.12.0/node-v22.12.0-linux-x64.tar.xz
#wget https://nodejs.org/dist/v20.18.1/node-v20.18.1-linux-x64.tar.xz
#wget https://nodejs.org/dist/v18.20.5/node-v18.20.5-linux-x64.tar.xz 


# Untar Node.js
tar -xvf node-v22.12.0-linux-x64.tar.xz
#tar -xvf node-v20.18.1-linux-x64.tar.xz
#tar -xvf node-v18.20.5-linux-x64.tar.xz


# Move Node.js to /usr/local
sudo mv node-v22.12.0-linux-x64 /usr/local/node
#sudo mv node-v20.18.1-linux-x64 /usr/local/node
#sudo mv node-v18.20.5-linux-x64 /usr/local/node


# Create symbolic links for node and npm
sudo ln -s /usr/local/node/bin/node /usr/local/bin/node
sudo ln -s /usr/local/node/bin/npm /usr/local/bin/npm

# Verify Node.js installation
node -v
npm -v
