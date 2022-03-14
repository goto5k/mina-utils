# mina-utils  
## Node auto restarter  
Automatically restarts container if node hangs  

Requirements  
`sudo apt install -y curl bc jq && sudo usermod -aG docker $USER`  


Simple run  
`curl -s https://raw.githubusercontent.com/goto5k/mina-utils/main/node-restarter.sh | bash`

Launch with notifications in telegram  
`curl -s https://raw.githubusercontent.com/goto5k/mina-utils/main/node-restarter.sh | bash -s -- <TG_TOKEN> <TG_CHAT_ID>`

Add it to cron:  
`crontab -l | { cat; echo "*/10 * * * * curl -s https://raw.githubusercontent.com/goto5k/mina-utils/main/node-restarter.sh | bash"; } | crontab -`
