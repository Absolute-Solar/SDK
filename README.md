# CryptoSun SDK
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
[![Latest Release](https://img.shields.io/github/v/release/Absolute-Solar/cryptosun-vote)]()

Client library and examples for dApps to interact with the CryptoSun program library. Application development on Solana blockchain etc.

# Technical Details
 
    Blockchain: Solana
    Throughput: ~65,000 TPS (peak 700,000 TPS)
    Cryptography: Ed25519 (128-bit security)
    Consensus: Proof of History (PoH) + Proof of Stake (PoS) + Tower BFT
    Programming: Rust, compiled to BPF bytecode
    Serialization: Borsh (150-200 byte tx size)
    Fees: Base 0.000005 SOL/signature, prioritization adjustable
 
# Smart Contracts
 
    Token: Defines CSN (100M supply, 9 decimals, 1M CSN/year minting).
    Staking: Locks 42M CSN, rewards via Reward = 0.0001 · Stake · (EnergyFactor + UptimeFactor + MaintenanceFactor).
    Governance: 4M CSN, vested Months 13-24, 2/3 vote consensus.
    Burn: Reduces supply (e.g., 3.5M CSN/year by Year 6).
    Dividend: Airdrops based on Dividends through Company revenue.
    Future: Maintenance (IoT-driven), Energy trading (LMP pricing).

# References 
<a>https://solana.stackexchange.com/</a><br>
<a>https://solana.com/docs</a><br>
<a>https://explorer.solana.com/</a><br>
<a>https://faucet.solana.com/</a><br>
<a>https://git-scm.com/book/en/v2</a><br>
<a>https://docs.rs/anchor-lang/latest/anchor_lang/accounts/account/struct.Account.html</a><br>
<a>https://blog.networkchuck.com/posts/create-a-solana-token/</a><br>
<a>https://docs.anza.xyz/cli/install</a><br>
<a>https://beta.solpg.io/</a><br>
<a>https://education.github.com/git-cheat-sheet-education.pdf</a><br>
<a>https://www.dialect.to/</a><br>
 
# Installation(Windows)
Ref: <a>https://learn.microsoft.com/en-us/windows/wsl/install<a>

    bash
    wsl --install
    wsl
 
Now follow the rest of the Linux installation
 
# Installation(Linux)
Download VS Code:
Ref: <a>https://code.visualstudio.com/download</a>
<br>
 
VS code Extensions:

    dependi
    crates
    dev containers
    docker
    github co-pilot
    github co-pilot chat
    github pull requests
    julia
    material icon theme
    pine script
    prettier code
    rainbow csv
    react native
    react-native/react
    rust
    rust-syntax
    rust-analyzer
<br>
 
Download Dependencies:

    Rust: cargo --version >= 1.70
    Solana CLI: solana --version >= 1.18
    Node.js: node --version >= 16 (for tools)
    Git: git --version
    Anchor CLI: anchor --version
<br>
 
Quick Install <a>https://solana.com/docs/intro/installation</a>

    curl --proto '=https' --tlsv1.2 -sSfL https://raw.githubusercontent.com/solana-developers/solana-install/main/install.sh | bash
<br>
 
Download Rust:

    curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y
<br>    
 
Run the following command to reload your PATH environment variable to include Cargo's bin directory:

    . "$HOME/.cargo/env"
<br>
 
To verify that the installation was successful, check the Rust version:

    rustc --version
<br>
 
Install the Solana CLI:
 
    sh -c "$(curl -sSfL https://release.anza.xyz/stable/install)"
<br>
 
Add Path variable: 

    export PATH="$HOME/.local/share/solana/install/active_release/bin:$PATH"
    solana --version
<br>
 
To update:

    agave-install update
<br>
 
Install Anchor CLI:
 
    cargo install --git https://github.com/coral-xyz/anchor avm --force
    avm --version
<br>
 
To Update: 

    avm install latest
    avm use latest
<br>
 
Node install:

    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/master/install.sh | bash
<br>

# Solana Basic Commands

    solana config get
    solana config set --url mainnet-beta
    solana config set --url devnet
    solana config set --url localhost
    solana config set --url testnet
<br>
 
Create a wallet: 
 
    solana-keygen new
    solana address
<br>
 
Airdrop SOL:

    solana config set -ud
    solana airdrop 2
    solana balance
<br>    
 
Run Local Validator:

    solana-test-validator
    solana config set -ul
<br>
 
# Setup(Bash)
 
<p>Clone Repo</p>
<p>Install dependencies</p>
<p>Set up Next.js</p>
<p>Set up Node</p>
<p>Configure Solana</p>
<p>Deploy Contracts</p>
<br>
 
Clone the Repository: 
 
    git clone https://github.com/rednickk1/CryptoSun.git
    cd CrytpoSun
<br>
 
Install Dependencies:

    cargo build --release
    npm install
<br>
 
Setting up Next.js Environment:
 
    npx create-solana-dapp
<br>
 
Configure Next.js:

    Project name:
    Preset:
    UI Lib:
    Anchor Template:
    cd /your-project-directory
<br>
 
Web Front End:

    npm i
    npm run dev
 
Will now be running on localhost: <a>http://localhost:3000</a>
<br>
 
# Setting up Solana Validator:
install phantom wallet
<a>https://phantom.com/</a>
<br>
 
Change to devnet or testnet then run on terminal:
 
    solana-test-validator
<br>
 
Configure Solana:

    solana config set --url https://api.devnet-beta.solana.com
    solana-keygen new
<br>
 
Deploy Contracts:
 
    solana program deploy target/deploy/csn_token.so
<br>
 
Usage:
 
    #![allow(unexpected_cfgs)] to avoid unwanted cfg errors
 
    Compile: cargo build 
 
    Test: cargo test
 
    Interact: Use Solana CLI or SDK (e.g., @solana/web3.js) to call contracts.
 
        Example: Transfer CSN
 
        javascript

        const { PublicKey, Transaction } = require('@solana/web3.js');
 
        // Add transfer logic here 
<br>

# Contributions
 
Contributing (Currently only Absolute Solars Dev Team possible open-source after Launch)
 
Open-source Devs! Please follow these steps:
 
//removed bullet points here//
 
Fork the repository and create a feature branch with your changes. Ensure code adheres to Rust best practices and Solana’s security standards. Submit a pull request with a clear description of your contribution. Issues can be reported via GitHub Issues—focus on bugs, feature requests, or security enhancements.
 
Security

    Audits: Conducted by CyberScope and CertiK or reputable sources.
    Bounties: Report vulnerabilities to earn $1,000-$50,000 (CSN).
    Contact: devnickk@proton.me
<br>

# License
This project is licensed under the MIT License. See LICENSE for details.
 
Resources
 
    Website: CryptoSun.ca
    Whitepaper: CSN Whitepaper
    Solana Docs: docs.solana.com
    Contact: devnickk@proton.me
    @Absolute Solar & Crypto inc.
