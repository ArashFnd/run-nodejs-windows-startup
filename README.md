# run-nodejs-windows-startup
If you want to deploy your node js app on a windows server, this documentation is for you

## 1) Install PM2 globally
  `npm install -g pm2`

## 2) Start your Node.js API
  Navigate to your API folder:
  `cd C:\path\to\your\api
  pm2 start app.js --name "my-api"`
