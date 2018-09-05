# Installation Instructions

## Get Docker

For the raspberry pi, these are the commands you need to execute

```aidl
curl -fsSL get.docker.com -o get-docker.sh && sh get-docker.sh
sudo apt install -y docker-compose
```
After cloning the git repo, and entering the directory, run

```aidl
sudo docker-compose build
```

# Make Discord Bot Account
https://discordapp.com/developers/applications/

Make a bot, and obtain a token.

# Make Reddit Bot Account

# Populate examples/config.py with both bot credentials

# Add channel ids to examples/config.py

# Move config.py outside of examples folder

# Run bot with docker-compose up in root directory
