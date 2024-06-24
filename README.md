# Eclipse-testnet-interaction

# REMEMBER, THIS IS ONLY FOR EDUCATIONAL PURPOSES! NOTHING IS PROMISED!  


__________________
## Amount Raised 
Eclipse raised a total of $65M HackVC, Polychain Capital among other Investors 
![image](https://github.com/Ravindrareddy161/Eclipse-testnet-interaction/assets/152148394/8a4dd070-ccb5-41d1-b48e-502d36100cf4)

----------------


## Gettings Started 
### Installing Perequisite 
```
sudo apt update
sudo apt upgrade -y
```


### Install Rust 

```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
Reply with ```1```
![image](https://github.com/Ravindrareddy161/Eclipse-testnet-interaction/assets/152148394/2494aee9-4be6-4280-8585-0735b0a34c7e)


### Environment Variable  

```
. "$HOME/.cargo/env"
```
![image](https://github.com/Ravindrareddy161/Eclipse-testnet-interaction/assets/152148394/b09510e6-1a77-47fb-a45f-5c3176509e36)


### check ```RUST version```

```
rustc --version
```


## Install Solana CLI 

```
sh -c "$(curl -sSfL https://release.solana.com/stable/install)"
```
![image](https://github.com/Ravindrareddy161/Eclipse-testnet-interaction/assets/152148394/7cc6bb0e-d274-496f-8ce2-f29719b94043)


```
export PATH="/root/.local/share/solana/install/active_release/bin:$PATH"
```
![image](https://github.com/Ravindrareddy161/Eclipse-testnet-interaction/assets/152148394/98ebb7b9-8608-424b-bd9c-fb75001f3105)


### check version if installed properly 
```
solana --version
```
![image](https://github.com/Ravindrareddy161/Eclipse-testnet-interaction/assets/152148394/649ddc90-0e57-44c9-9892-dfd5d65df5c1)




### Install dependencies 
Reply with ```y``` and proceed 
```
sudo apt-get update
sudo apt-get install nodejs
sudo apt-get install npm
npm install --global yarn

```


### Checking version 
```
node -v
npm --version
yarn --version
```
![image](https://github.com/Ravindrareddy161/Eclipse-testnet-interaction/assets/152148394/2286f10a-0298-45a7-9003-e5c549259d56)



# Install Anchor 

```
cargo install --git https://github.com/project-serum/anchor anchor-cli --locked
```
![image](https://github.com/Ravindrareddy161/Eclipse-testnet-interaction/assets/152148394/555205ae-31cf-456f-9784-4d03728a385f)


-------------------

### Check version 
```
anchor --version
```
------------


## Create a Solana Wallet 
```
solana-keygen new -o /path-to-wallet/my-wallet.json
```
![image](https://github.com/Ravindrareddy161/Eclipse-testnet-interaction/assets/152148394/a97b94b0-6fe4-4f17-92e3-4fca382484b0)


Press ```ENTER``` ans save the Info 
![image](https://github.com/mztacat/Eclipse-Testnet-Interaction/assets/31314340/dc67db2f-e5aa-44d6-b033-882a96573d0c)




## Update configuration to use new wallet
```
solana config set --url https://testnet.dev2.eclipsenetwork.xyz/
```
![image](https://github.com/Ravindrareddy161/Eclipse-testnet-interaction/assets/152148394/9ba2d329-5e19-4148-b02c-b84848e6917e)

```
solana config set --keypair /path-to-wallet/my-wallet.json

```

### Save Solana address 
```
solana address
```


-----------------------

# Import the same seedphrase to Metamask/Rabby Wallet --- for we are gonna send Ethereum Sepolia to it 
## I renamed it so i won't mix it up with my wallet 

![image](https://github.com/Ravindrareddy161/Eclipse-testnet-interaction/assets/152148394/211c101d-9fae-4467-b948-c09887fd1fc8)

### Request Sepolia gas on your main wallet: 
MINE SEPOLIA GAS  ---https://sepolia-faucet.pk910.de/
Request from Quicknode ---  https://faucet.quicknode.com/ethereum/sepolia 
![image](https://github.com/Ravindrareddy161/Eclipse-testnet-interaction/assets/152148394/31b9acd2-fdda-40d9-8324-cefa102b2c54)
![image](https://github.com/Ravindrareddy161/Eclipse-testnet-interaction/assets/152148394/208bd1be-3cf7-4af8-9288-594275630a2b)




---------------------
### Send Sepolia ETH to the wallet imported 
![image](https://github.com/mztacat/Eclipse-Testnet-Interaction/assets/31314340/9658de88-4fa4-47a5-b667-21ea2db684f6)

---------------



# Clone Eclipse Bridge Script 

```
git clone https://github.com/Eclipse-Laboratories-Inc/testnet-deposit
```
![image](https://github.com/Ravindrareddy161/Eclipse-testnet-interaction/assets/152148394/38685176-f2e6-4784-9518-851f358d01d5)


### Navigate to ```testnet-deposit```
```
cd testnet-deposit
```

```
npm install
```
![image](https://github.com/Ravindrareddy161/Eclipse-testnet-interaction/assets/152148394/b54ed6b6-2135-4e3a-8f8e-3e887d0e6acc)



# AMENDEMENT BEFORE WE PROCEED 
Update Node version 
```
sudo apt-get remove nodejs
```
press `y``` and proceed 


```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
source ~/.bashrc
```

```
nvm install --lts
nvm use --lts
```

```
node -v
```
![image](https://github.com/Ravindrareddy161/Eclipse-testnet-interaction/assets/152148394/6e94a926-dfdf-4ca0-899c-c70ca4f4cd9f)



## Run Bridge script 

```
node deposit.js [Solana Address] 0x7C9e161ebe55000a3220F972058Fb83273653a6e [Amount in Gwei] [Fee in Gwei] [Ethereum Private Key] [Sepolia RPC Endpoint]
```

### Repalce solana address with the one you coped alonside the seedphrase
### Amount in GWEI ```3000000```
### Fee in GWEI ```100000``` 
### Private key [view the private key of that seedphrase imported in Rabby wallet and paste 
### Sepolia RPC ```Endpoint```  -- https://rpc.sepolia.org/ 


------------------
### E.g  End product will look like this 
```
node deposit.js Cz2CCCtzqUAB97NAkVM6FzdF6d3EPx7pa4pN1JaWwrxz 0x7C9e161ebe55000a3220F972058Fb83273653a6e 3000000 3000000 0xeeeeeeeeeeeeeeeeeeprivatekey https://rpc.sepolia.org/
```
![image](https://github.com/Ravindrareddy161/Eclipse-testnet-interaction/assets/152148394/56434e13-9ba7-4c47-a574-e7b649d67b22)

### REPEAT PROCESS 3 - 4 TIMES 


## Ckeck balance 
```
solana balance
```
![image](https://github.com/Ravindrareddy161/Eclipse-testnet-interaction/assets/152148394/7bd8aa55-0fc0-484f-a72d-39d8b20c6a61)


------------------
# Creating a Token 
```
spl-token create-token --enable-metadata -p TokenzQdBNbLqP5VEhdkAS6EPFLC1PHnBqCXEpPxuEb
```
![image](https://github.com/Ravindrareddy161/Eclipse-testnet-interaction/assets/152148394/3f68a2d2-7aeb-4b9a-bb85-b4c426103b12)



## Mint Token 
```
spl-token create-account <YOUR_TOKEN_ADDRESS>
```

### Replace with your token address previously deplyed from above step 
![image](https://github.com/Ravindrareddy161/Eclipse-testnet-interaction/assets/152148394/a5c9c9ee-e6a6-4c99-9ffa-540feb5242da)


### Mint token
```
spl-token mint <YOUR_TOKEN_ADDRESS> 10000
```
![image](https://github.com/Ravindrareddy161/Eclipse-testnet-interaction/assets/152148394/ec35a013-bba4-46ab-93d1-21a03c590f26)


### Check token balance 
```
spl-token accounts
```
![image](https://github.com/Ravindrareddy161/Eclipse-testnet-interaction/assets/152148394/a0b1e7f0-268e-4f63-ba85-35e20fa4d6e0)



# DONE! !!

# THAT'S ALL FOR NOW, REMEMBER, THIS IS ONLY FOR EDUCATIONAL PURPOSES! NOTHING IS PROMISED! 






Fill form: 
https://docs.google.com/forms/d/e/1FAIpQLSfJQCFBKHpiy2HVw9lTjCj7k0BqNKnP6G1cd0YdKhaPLWD-AA/viewform?pli=1

![image](https://github.com/Ravindrareddy161/Eclipse-testnet-interaction/assets/152148394/38c454a2-f179-454b-abb0-04e611c847ff)











---------------



