# Reddio Testnet Bot

<div align="center">

```
██████╗ ███████╗██████╗ ██████╗ ██╗ ██████╗     ██████╗  ██████╗ ████████╗
██╔══██╗██╔════╝██╔══██╗██╔══██╗██║██╔═══██╗    ██╔══██╗██╔═══██╗╚══██╔══╝
██████╔╝█████╗  ██║  ██║██║  ██║██║██║   ██║    ██████╔╝██║   ██║   ██║   
██╔══██╗██╔══╝  ██║  ██║██║  ██║██║██║   ██║    ██╔══██╗██║   ██║   ██║   
██║  ██║███████╗██████╔╝██████╔╝██║╚██████╔╝    ██████╔╝╚██████╔╝   ██║   
╚═╝  ╚═╝╚══════╝╚═════╝ ╚═════╝ ╚═╝ ╚═════╝     ╚═════╝  ╚═════╝    ╚═╝   
```

<a href="https://t.me/divinus_xyz">
    <img src="https://img.shields.io/badge/Telegram-Channel-blue?style=for-the-badge&logo=telegram" alt="Telegram Channel">
</a>
<a href="https://t.me/divinus_py">
    <img src="https://img.shields.io/badge/Telegram-Contact-blue?style=for-the-badge&logo=telegram" alt="Telegram Contact">
</a>
<br>
<b>Donations:</b> <code>0x63F78ecCB360516C13Dd48CA3CA3f72eB3D4Fd3e</code>
</div>

A multifunctional bot for automating quest completion in Reddio Testnet.

## 🚀 Tasks that the software performs

- Account Registration and Management
  - Full automatic registration with Reddio Testnet
  
- Web3 activities
  - Test token acquisition through faucet
  - Token transfer to random wallets
  - Token bridging from Sepolia to Reddio
  - Deployment of unique custom ERC20 tokens

- Social Network tasks
  - Twitter tasks (following, retweeting, add "Reddio" in Username and Bio)
  - Twitter account bind
  - Discord account bind

- Verification of task completion
  - Checking the last verification
  - Verification quests to gain XP

## 🌐 Supported Networks

- Reddio Testnet - Main operations environment
- Sepolia Testnet - For bridging operations
- Multi-wallet and proxy support
- EVM-compatible operations

## 📋 System Requirements

- Python 3.10+
- Windows/Linux
- Twitter account
- Discord account

## 🛠️ Installation

1. Clone the repository:
```bash
git clone [repository URL]
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # Linux
.\venv\Scripts\activate   # Windows
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

## ⚙️ Configuration

### Required Configuration Files

Create and populate these files in the `config/data/client/` directory:

#### private_keys.txt
```
private_key
private_key
...
```

#### auth_tokens_twitter.txt (for Twitter tasks)
```
auth_token1
auth_token2
...
```

#### auth_tokens_discord.txt (for Discord tasks)
```
discord_token1
discord_token2
...
```

#### proxies.txt (optional but recommended)
```
login:password@ip:port
login:password@ip:port
...
```

### settings.yaml Configuration

```yaml
# Threading Configuration
threads: 1

# Network Settings
reddio_rpc: https://reddio-dev.reddio.com
reddio_explorer: https://reddio-devnet.l2scan.co

sepolia_rpc: wss://ethereum-sepolia-rpc.publicnode.com
sepolia_explorer: https://sepolia.etherscan.io

# Timing Settings
delay_before_start:
    min: 0
    max: 0

# API keys for captcha solving
cap_monster: ""

# Tokens list
tokens:
  - name: STT
    address: ""
  - name: WSTT
    address: ""
  - name: USDT
    address: ""
  - name: WBTC
    address: ""

# Referral code for registration
referral_code: ""
```

### Twitter Setup

1. Log into your Twitter account
2. Open Developer Tools (F12) -> Application -> Cookies
3. Find and copy the `auth_token` value
4. Add it to `config/data/client/auth_tokens_twitter.txt`

### Discord Setup

1. Extract your Discord token from browser or Discord client
2. Add it to `config/data/client/auth_tokens_discord.txt`

## 🚀 Usage

To start the bot:

```bash
python run.py
```

### Available Modules

1. 📱 Registration Account - Register and set up profile with Reddio
2. 🚰 Faucet - Claim test tokens from faucet
3. ✈️ Transferred - Transfer tokens to earn XP
4. 🏗️ Contract Deployment - Deploy your own ERC20 token for XP
5. 💱 Bridged - Bridge tokens from Sepolia to Reddio
6. 🐥 Twitter tasks - Complete Twitter-related tasks for XP
7. 🎮 Discord tasks - Complete Discord integration for XP
8. 🚪 Exit - Close the application

## ⚠️ Module Details

### Registration Account
Registers a new account, connects social networks, and sets up your profile.

### Faucet
Requests test tokens from the Reddio testnet faucet once every 24 hours.

### Transferred
Transfer tokens to a random wallet available once every 24 hours.

### Contract Deployment
Deploys a randomly generated ERC20 token contract.

### Bridged
Bridges tokens from Sepolia to Reddio testnet.

### Twitter Tasks
Completes Twitter-related quests:
- Follow Reddio account
- Retweet specified tweet
- Add "Reddio" to username and bio

### Discord Tasks
Connects your Discord account to Reddio platform.

## 🔒 Security Recommendations

1. **Wallet Security**:
   - Store private keys securely

2. **Proxy Usage**:
   - Use reliable proxy services to avoid IP blocking
   - Verify proxy functionality before running tasks

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📜 License

This project is distributed under the MIT License.

## ⚠️ Disclaimer

Use the bot at your own risk. The author is not responsible for any consequences resulting from the use of this software, including account restrictions or loss of funds. This software is designed for educational purposes and legitimate testnet interaction only.
