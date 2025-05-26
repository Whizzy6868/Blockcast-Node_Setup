# Blockcast-Node_Setup
Simplest way I am running a Blockcast Node
### First Singup 
Click here https://app.blockcast.network?referral-code=FmeAOt
Singup, connect your SOL wallet (New),
Connect your Discord and 
Connect your X
### Download Docker Desktop
Personally I like using the docker desktop to avoid cli errors,
Incase you encounter wsl errors here are some ways to fix it,
https://github.com/docker/for-win/issues/14540#issuecomment-2599495618
When you are done open your docker desktop on.
### Node Requirement
Requirements (Minimum 2 CPU cores and 4GB RAM )
### Update system & dependencies 
```
sudo apt update && sudo apt upgrade -y
```

```
sudo apt install ca-certificates curl gnupg lsb-release -y
```
### Add Docker Key

```
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

```

```
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] \
  https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

### Clone Blockcast Repo 
```
git clone https://github.com/Blockcast/beacon-docker-compose.git
cd beacon-docker-compose
```

### Run Node 
```
docker compose up -d
```
### Check running container 
```
docker ps
```
### Get Hardware ID & Challenge Key
```
docker compose exec blockcastd blockcastd init
```
###### You'll see output like `Hardware ID: your-hardware-id` and `Challenge Key: your-challenge-key`

## Register Your Node
Visit Blockcast Website, https://app.blockcast.network?referral-code=FmeAOt 

Signup/sign in using email,
Click the Manage Node and Register Node,
Paste your Hardware ID and Challenge Key

### SUBMIT AND DONE
Always have a 24/7 uptime 
