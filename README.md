## INVITE
https://discordapp.com/oauth2/authorize?client_id=247869756609265664&scope=bot&permissions=0

## USAGE/DEPLOYMENT

### Docker
Copy the Dockerfile to your local system with Docker installed and build the image like this:  
`docker build -t trump-bot .`

Afterwards, run the image via executing:  
`docker run trump-bot --env token=<your-token-here>`

Your container should come up and start deploying shards. 

### Custom environment installation

#### Download/Clone the bot
`git clone https://github.com/Blogshot/trump-bot.git`  
`git checkout js_conversion` 

#### Install Nodejs
https://nodejs.org/en/download/

```
curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
sudo apt-get install -y nodejs
```

#### Install Python 2.7 (3.x is not supported by some dependencies \[at time of writing\]!)
https://www.python.org/downloads/release/python-2714/

### Install FFMPEG.

#### Debian/Ubuntu
`apt-get install ffmpeg`

#### Windows
[edit your environment variables](http://adaptivesamples.com/how-to-install-ffmpeg-on-windows/)

#### Other OS
Download the appropriate package from here: https://ffmpeg.org/download.html

### Create a file named `stats.json` to store statistics
```
{
  "guildCount": 0,
  "shards": 0
}
```

### Create a file named `config.js` to store configuration data (the bot-token)
```
module.exports = {
  // https://discordapp.com/developers/applications/me
  token: "<bot-token>"
};
```

### Initialize NPM
`npm init`  

### Install basic packages
`npm install --global --production windows-build-tools` (Windows only)  
`npm install discord.js node-opus@0.2.9` 

#### Optional
For best experience, you may choose to install the following packages:  
`npm install bufferutil@3.0.5 (much faster websocket connection)

### Start the bot

#### Without sharding
`node bot.js`

#### With sharding
`node sharder.js`
