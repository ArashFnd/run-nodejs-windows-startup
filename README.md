# run-nodejs-windows-startup
If you want to deploy your node js app on a windows server, this documentation is for you

## 1) Install PM2 globally
  ```bash
  npm install -g pm2
  ```

## 2) Start your Node.js API
  Navigate to your API folder:
  ```bash
  cd C:\path\to\your\api
  pm2 start app.js --name "my-api"
  ```
  (Replace app.js with your API entry file.)

## 3) Save the PM2 process list
  ```bash
  pm2 save
  ```

## 4) Generate and enable PM2 startup script
  Run:
  ```bash
  pm2 startup
  ```
  It will print a command like:
  ```bash
  [PM2] To setup the startup script, copy/paste the following:
  pm2-startup install
  ```
  or
  ```bash
  powershell -Command "pm2-startup install"
  ```
  Copy and paste that line exactly into PowerShell (as Administrator).

## 5) Reboot test
  Reboot your server and check if your API started automatically:
  ```bash
  pm2 list
  ```
  You should see your app running ✅.

## 🔄 Useful PM2 commands
  - `pm2 restart my-api` → Restart API
  - `pm2 stop my-api` → Stop API
  - `pm2 delete my-api` → Remove from PM2
  - `pm2 logs my-api` → Tail logs

