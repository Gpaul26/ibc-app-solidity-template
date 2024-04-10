## Brigde Lottery contract using Polymer IBC

## Usage

### Requirement
1. Create a new `.env` file(clone from `.env.example`), update those environments
```
PRIVATE_KEY_1=''
# Add more if your project requires more private keys

# API keys for developer tooling and infra
OP_ALCHEMY_API_KEY=''
BASE_ALCHEMY_API_KEY=''
OP_BLOCKSCOUT_API_KEY=''
BASE_BLOCKSCOUT_API_KEY=''

```
2. Install node_modules
```
npm install 
```
3. Install Foundry `https://book.getfoundry.sh/getting-started/installation`
4. Build contract
```
forge build
```

### Steps
1. Set Contract

```bash
npx just set-contracts optimism BridgeLottery false && just set-contracts base BridgeLottery false
```

2. Deploy Contracts(in optimism, base network)

```bash
npx just deploy optimism base
```

3. Verification to ensure that configuration files align with your deployed contracts

```bash
npx just sanity-check
```

4. Create new Channel

```bash
npx just create-channel
```

5. Try to send packet

```bash
npx just send-packet optimism
```