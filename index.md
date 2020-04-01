# Juice Shop

An intentionally insecure webapp suitable for pentesting and security awareness trainings written in Node, Express and Angular. Inspired by the "classic" [BodgeIt Store](https://code.google.com/p/bodgeit/) by [@psiinon](https://github.com/psiinon).

> Translating "dump" or "useless outfit" into German yields "Saftladen" which can be reverse-translated word by word into "juice shop". Hence the name of this project.
    
You may find it easier to find vulnerabilities using a pen test tool. I strongly recommend [Zed Attack Proxy](https://code.google.com/p/zaproxy/) which is open source and very powerful, yet beginner friendly.
 
## Features

- Easy to install: Just requires [node.js](http://nodejs.org)
- Self contained: Additional dependencies will be resolved and downloaded automatically
- No external DB:  A simple file based SQLite database is used which is wiped and regenerated on server startup
- Open source: No hidden costs or caveats
 
## Getting started

### From Sources

1. Install [node.js](http://nodejs.org) (version 0.10.x)
2. Run ```git clone https://github.com/bkimminich/juice-shop.git``` (or clone [your own fork](https://github.com/bkimminich/juice-shop/fork) of the repository) 
3. Run ```npm install``` (only has to be done before first start or when you change the source code)
4. Run ```npm start```
5. Browse to <http://localhost:3000>

### Docker Container

1. Install [Docker](https://www.docker.com)
2. Run ```docker pull bkimminich/juice-shop```
3. Run ```docker run -d -p 3000:3000 bkimminich/juice-shop```
4. Browse to <http://localhost:3000> 

### Packaged Distribution

1. Install [node.js](http://nodejs.org) (version 0.10.x)
2. Download ```juice-shop-<version>.zip``` attached to [latest release](https://github.com/bkimminich/juice-shop/releases/latest)
3. Unpack and run ```npm start``` in unzipped folder
4. Browse to <http://localhost:3000>

## Troubleshooting

- If you are experiencing [Error 128](https://github.com/bower/bower/issues/50) from some GitHub repos during ```bower_install.js``` execution, run ```git config --global url."https://".insteadOf git://``` and try ```npm install``` again
- If using Boot2Docker (Docker inside VirtualBox on Windows) make sure that you also enable port forwarding from Host ```127.0.0.1:3000``` to ```0.0.0.0:3000``` for TCP 
- If ```npm install``` fails after an update of your local copy during ```bower_install.js``` complaining about version issues, delete ```/app/bower_components``` and try again to remove outdated versions that cause conflicts