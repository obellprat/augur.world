# Augur.world
AUGUR is an initiative of the Swiss Agency for Development (SDC) humanitarian innovation accelerator “Innovation meets Practice” in 202 - see [pitch deck]([https://augur.world/home](https://static1.squarespace.com/static/619fa4f7993ee055dc490d70/t/61cc627e1ac49e69c79a5e22/1640784527710/presentation_augur_pitch_final.pdf)) 

Its vision is to provide state-of-the-art information on climate disasters and change which is open source, quality proven and feasible for humanitarian actors. These services reduce the financial and administrative costs to access climate expert knowledge.

AUGUR combines information from satellite imaginary and climate change modelling. A first product is the development of a digital toolkit to assess the risk from heavy precipitation. Additional products will offer the calculation of riverine discharge and level of flooding for remote areas where no local and global trust worthful data is available.

Access to the the [AUGUR prototype toolkit](https://augur.world/home) 

# Tooling Info for augur.world
- JavaScript runtime: [NodeJS](https://nodejs.org/)
- Web Server Framework: [ExpressJS](https://expressjs.com/)
- Database: [sqlite](https://sqlite.org/index.html)
- Web build tool: [ParcelJS](https://parceljs.org/)

# Preperation
- Install nodeJS https://nodejs.org/ (>16)
- Install yarn package manager via npm (bundled with nodeJS)
```shell
npm install --global yarn
```

# Installation

- Clone repository and go to client
```shell
cd augur.world
cd client
```

- Create .env file with content
```shell
cat -env "SERVER=http://localhost:3000/api"
npm install
npm run build
npm run start-server
```

- Note that http://localhost:3000/api is the endpoint for api, so if you start your server in a different port you need to set it accordingly, or in production, just set the actual url.
- Go to main folder, then
```shell
cd server
```

- Create .env file with content
```shell
PORT=3000
DB_PATH=/Users/gaskar/Documents/augur.sqlite
npm install
npm start
```

# Run Application
```shell
pm2 start "npm run start-server" --name client
pm2 start --name server server.js
```

# Open Application
Open your Web browser and go to http://localhost:1234/
