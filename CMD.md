
## Server
### Create a new project
```bash
pnpm init
```

### Install dependencies
```bash
pnpm add fastify fastify-socket.io ioredis close-with-grace dotenv socket.io @fastify/cors
```

### Install dev dependencies
```bash
pnpm add @types/node tsx typescript @types/ws -D
```

### Create tsconfig.json
```bash
pnpm tsc --init
```
## UI
### Create Next.js app
```base
pnpm create next-app ui
```

### Install dependencies
```bash
pnpm add socket.io-client
```
### Install dev dependencies
```bash
pnpm add @types/ws -D
```

### Install shadcn-ui
```bash
npx shadcn-ui@latest init
```


### Add components
```bash
npx shadcn-ui@latest add textarea button form
```


## Deploy steps
### Create the server
1. Generate some keys https://www.wpoven.com/tools/create-ssh-key#
1. Create a DO droplet

### Configure the server
1. SSH intro droplet
1. Update the package repository metadata - sudo apt update
1. Add the NodeJS package - `curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -`
1. Install Node.js `sudo apt-get install nodejs`
1. Install docker compose - `sudo apt install docker-compose`
1. Install NodeJS (so we can build the UI) - `sudo apt install nodejs npm`
1. Install pnpm - `wget -qO- https://get.pnpm.io/install.sh | sh -`
1. `source /root/.bashrc`
1. If you're using a private repo get a GitHub PAT
1. Clone the repo - git clone `https://<PAT>@<repo>`

### Start deploying
1. Configure the GH action