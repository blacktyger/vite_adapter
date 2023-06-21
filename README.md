# vite-wallet-adapter
Manage VITE Blockchain API via @vite.js NODE.JS package within Python script

### Requirements
- Node.js and npm
- Python 3.11

### Installation
- clone the repository
- `cd vite-wallet-adapte\vitejs`
- `npm install`

### How to use
```python
from vitejs_adapter import ViteJsAdapter

provider = ViteJsAdapter()

# Create new wallet and return dict with address and mnemonics
wallet = provider.create_wallet()

# Get the wallet balance using address and/or mnemonics
print(provider.balance(address=wallet['data']['address']))

# Get list of wallet transactions using wallet address
print(provider.transactions(address=wallet['data']['address'], page_size=10, page_index=0))
```