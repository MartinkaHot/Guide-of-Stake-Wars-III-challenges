# Guide-of-Stake-Wars-III-challenges# Challenge 001

### Create a wallet
I guess it's simple enough as usual. Press the buttons and most importantly save the memory phrase.

[https://wallet.shardnet.near.org/](https://wallet.shardnet.near.org/)

After creating a wallet I received 50 tokens on my balance. Next we will order a VPS server and move on to the most difficult part of the installation.

I order my favorite provider VPS on Hetzner. CPX31 will be enough for our needs. It cost near 15 dollars per month.


#### Installing NEAR-CLI

    sudo apt update -y && sudo apt upgrade -y

![](https://lh4.googleusercontent.com/ow9qaqslC0caFbZRCo-ZCC7U2bV9P7T6rPxGSKeHi3RrWzfCiIXqL8012y6ej_fL6Ag1a1ZfkI5LEhKVabVGQH4L4IhmTGML_ipwqtADnNaBjQ1jopwe0aJE_1GmWoVi2e_Lz_kADjnHjUTEbrCpzQo)

![](https://lh6.googleusercontent.com/oaB40QHXOb6AJVRv2fdScMa6p6VxJ9IbzMijuPpugSL8N69WdR6C_OOSU41z4f7bTq5p47hiKFjqSDImkyaFCFK1wpXr0Y-bVVikHSWZwLqsQdiyAm7YDdYgz2ZzJRZ-HBCa3izFhY0MwPvAyWkL8vY)

##### Installing Node.js, and npm

    curl -sL https://deb.nodesource.com/setup_18.x | sudo -E bash -
    
    sudo apt install build-essential nodejs -y
    
    PATH="$PATH"

![](https://lh4.googleusercontent.com/0j4CNhFo5M4f0mpqtcmqZAWPlpFhVlE_2n7zWoOGRItPwcv_LU_llCD-nWih9PYo710oOMyK2Mc1bnKMRoDXbPPp7QqFSNe1635uS1cbWv9Y4D30ITXQN81Jz_Zpy5M7BWSCkL3tyemTztltPczl5Vg)

  

**Check version node.js and npm**

    node -v
    npm -v

![](https://lh4.googleusercontent.com/x9g0wxMddoOeRcpwZ4Lb2J8MYvPvR0kVwEFm1ggJh3CVW0RCynzUA9GkdMAGlr_kanFwMtocb_OlSuV5B9zZgdjTyiuiS3Rg4JUN1s443XYm1NVMtNynCx7lW-UEPhDisQoQT-5NHaf-D1ttTWniw6o)

#### Installing NEAR-CLI

    sudo npm install -g near-cli

![](https://lh3.googleusercontent.com/KRbWqj0oYG5drmTZR43NtRmrEyNhAyaz-H-qfLilPvqqukr-YDAkwYs0UMTeRIeZe6JEQVOxVocyCjRsHRWM06zf6DB2Ggb8_grmL0gNA66ra_tct8bBNwkWesmz01xNb75IS0mIPhgtkIp-0_AxnOA)

  

### Validator Stats

    add network
    export NEAR_ENV=shardnet
    echo 'export NEAR_ENV=shardnet' >> ~/.bashrc
    echo 'export NEAR_ENV=shardnet' >> ~/.bash_profile
    source $HOME/.bash_profile

![](https://lh3.googleusercontent.com/9z3CRw_ngMBJBqpCigpdZuwHbIRz9-_QO3b1Q3XgC37TkGjpcdeMnimIRXLi4rmL05wovmKO8susc8ocFcKl3ntxELZlbGo-KlEMQyWoSSNOAuiWy_mIQ81QNIYiAfaFp1BwiL0PdMtJdHt0i8t5r5k)
# Challenge 002

**Checking confirm CPU**

    lscpu | grep -P '(?=.*avx )(?=.*sse4.2 )(?=.*cx16 )(?=.*popcnt )' > /dev/null \
    && echo "Supported" \
    || echo "Not supported"

![](https://lh5.googleusercontent.com/jRHOy_GFnWuCAKzSsE4zjBw8SwPzGHRRtouS3892IbFHfJSg0IH4gLsOWFrVBPMCPx_kQoDblUgtp_GOKFO3xLBIPK7jYRi-hKC97jfOHA94QijImivSQlzDuPEjaHXUecv_DQiS1EbWBaiVNiSAFio)
**Installing developer tools**

    sudo apt install -y git binutils-dev libcurl4-openssl-dev zlib1g-dev libdw-dev libiberty-dev cmake gcc g++ python docker.io protobuf-compiler libssl-dev pkg-config clang llvm cargo

![](https://lh6.googleusercontent.com/5aWnkmU66htIOL5epcLv18E9kInnIaOOcbUXkL8oHKuC4Dpjl2S_k4yuUgKWJc-8uMiIHvHuVtDysIFZqbTxVuUASJh9bRzfcG4hnf3EWZLaZ32EZKuDRhvKzSOqgEyUQCiuhuVBtTQRALFEElDvmqA)
**Installing python pip**

`sudo apt install python3-pip -y`![](https://lh4.googleusercontent.com/lIlCKwD2rbIWeLFZyuDFlc0xD-5Ci0mbHOIGXAWTAY67lTUjJ5LmWl5cXqn6QBOZDxkfweeP8ticU_9k60iJ6MffMAO30cemDf1aPldOO2pNbvEK1UE9AsayGfRNgvnuZtKV19LsMRdA2jYrc2c7J3U)
**Seting the configuration**

    USER_BASE_BIN=$(python3 -m site --user-base)/bin
    export PATH="$USER_BASE_BIN:$PATH"

![](https://lh3.googleusercontent.com/Yvawn9c4Us6tl9TMsDctE8yVh3SAPzYA96wXtL53e61Yc_Cz8aG_wlqanqxwKcjLtO9qC0NDobc86LVI18SVwC87gOTCzcg3ookDnUXL37XVTQkbRJ-ksQT8afmBtZv1pHHQhChKnIPCp3oIzQY8Ybc)
**Installing Building env**

    sudo apt install clang build-essential make

![](https://lh4.googleusercontent.com/iqaE8Snw-W5We18AhphOuDj7nRncjBmgPAg7zJJoW8XErLaEe9CBf_6shX0mY0Gt3K7OaWyQBx2yAq3JIqUwKoySekNg1TYmL0YauSL1BECSBW-i2l2t4XBOr6Rr8agazVWFGcYNhMwR3ct_nV_gOUQ)

##### Installing Rust & Cargo

    curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

![](https://lh5.googleusercontent.com/B3MAqkfNXJvxpwDkRIw_AuR20Wk1oqxHR8Kd8uMMwTgBVpI6qicH-tw4pjp7aE-aZImIHtZf9WkmLJQUMaTEvwFBv4ShJmyIIDerE2TUTHN7F1OYwGG8Cb2PruXt8oWcOfttLpm3WPhNuUWMHTnBqU0)

    source $HOME/.cargo/env

  

#### Cloning nearcore project from GitHub and Checkout to the commiting

    git clone https://github.com/near/nearcore

  

![](https://lh6.googleusercontent.com/LZtCgambj3_RVvLHK44sc9SvgossZxDnRxszlaftMukgYQTH_Pi3w3myrIGatwL64o4PUuD_hKbD-QBfRzm9uiujBwSKDbqXcU3GcqkCdFc9rPNxZLX_ha5iw4z2tWtKrvCWWCHs8wkUK1D55idwUjA)

    cd nearcore
    git fetch
    git checkout 68bfa84ed1455f891032434d37ccad696e91e4f5


![](https://lh3.googleusercontent.com/wVNnIEb_-T995vrSpHR7D_lp46anehEkS9-1PTuVL0IZ0yWGOxAbpMKKAMIDJPQMkfsuwd25YWrMowcR_IeMAJBp5OnNh-_I5RXqFXDSk-HXgIYtjfiueTdcIb1uDIufD_z6kFTyCmwZGkki-AX5ETE)
  
#### Compiling nearcore binary

    cargo build -p neard --release --features shardnet

![](https://lh5.googleusercontent.com/9i60tuJr-pkgCko48JC5PN94O44X155-degGlkUZlgqE1wtryN2WeMcygGCHuWvXASj8j6zS9oRMW584O7P2YQ4rKknEIRlS4J60VHl5VGP5n0Ze0nfE629YLNXAif57RxwdDEb-8qwdcUwAeKR6TfQ)

#### Initialize working directory download-genesis

    ./target/release/neard --home ~/.near init --chain-id shardnet --download-genesis

![](https://lh5.googleusercontent.com/qW-6ZkQpcLRq_8kR-8D1DpCCf4ErnCCWc4E8i-8XzqyayQcGqCYhOMyuwKBgEOKi9I4WvKC2okYrFjkOOn8wB4Zmws3oyELwNg85dltNZg3iJXvlxEINbR8Lq7feaQC9ZoOZWD_gRYv_KMIFCdC9C80)

#### Replace the config

    rm ~/.near/config.json
    
    wget -O ~/.near/config.json 
    https://s3-us-west-1.amazonaws.com/build.nearprotocol.com/nearcore-deploy/shardnet/config.json

  

![](https://lh4.googleusercontent.com/ygp9HT-zv7M3tHxGDMMmBTmzi3NaxeLZgCqIY-Q83S4KlErnQJdm9Qvsg2oSD6N4DuDGhP0AC2VWzrFVj6ezjpoJm0YMzPhb1oGeMYPY5M4odMVukFrxY0HYtAEN2cQnLwgFBBXzsajJx9N4PpN1Cfg)

**Installing AWS Cli**

    sudo apt-get install awscli -y

![](https://lh5.googleusercontent.com/P4rouA8JhHv6jGzNx4MXG0xB_ZholtM1K-bo1BK385nfSUwcmE9_Bv2SOvBVsMMwG1a9MBNc_ggE4LZ-k92Rs3_cyZgP2gJHySQrlNZxbGfVB8-szTTrzyAWInYTaSiYPLYZp7nvijAXG5GsiG_sZlI)

**Downloading snapshot (genesis.json)**

    cd ~/.near
    wget https://s3-us-west-1.amazonaws.com/build.nearprotocol.com/nearcore-deploy/shardnet/genesis.json

![](https://lh6.googleusercontent.com/JV4s1RFTZ9t3QOJjP5xy4K-5-vjCdzR6178tGGbcwxAtQQf9sLdGdKAu1P2RVCFDtluc5pCC5iNToAUebS_4h4a_0DqJ0Gx979EHdV0YqYFspGvBgakItIc8yT6VIEV9uc9vK7v-F45gDieFaiWz6P8)

#### Runing the node—-

    cd ~/nearcore  
    ./target/release/neard --home ~/.near run

![](https://lh3.googleusercontent.com/ts0F88apo5Ta2cr9CTTzyF9fKu7BSVenmo9cLHZjLHGHGmBu6EAQo2CE-UvMKeYzc9EDc2Zns1IDKZ3HobmZ3mo2gjiTxyK-Aub8CqGGQ0mLSpxAszdjis92Mg_iVHMhhOrUuoKTMOflHmj20vNZLpg)

### Activating the node as validator

near login

1 Copy the link in your browser
2 Grant Access to Near CLI
3 After Grant, you will see a page like this, go back to console
4 Enter your wallet and press Enter![](https://lh6.googleusercontent.com/YMSd7YEacMeYHMz98OqRjwRMcc7j1b-daPWldYeTPxY75lDX3oqaJUy4yG7Nb7N_fj6_KGHdKMgpqUgwfk6MK-eR8UJN2QmsNUWd-uPm4GgPQdrzNz1sALvszbR51JatzK7OTShWtd-8wFx4lS5eWGE)

![](https://lh6.googleusercontent.com/QGXyguMNScNTCLnIyTeR8to3_Xghrry8WTUQGgpa8sPHHALTG-xxO-jRUIvZXvW4DsaPNmFEXehNGTmfNr78xdL9qydkDJGnVZXG50n6cyVrP01cTE7EuoQxxvYk4JRQ-ALoEnwULe8juhIdsmdRwkY)

![](https://lh5.googleusercontent.com/ygxC2disna9OpE_t9hUfmtTG7fovZKISiJEkuU58AC69ZvOoLuCmNO_Hn3aFzNohbjXxn6QlcnxxphO939nGtgndA4jcWJ0hxYQomrv08d2PCDszzJs8XhpeNQRTugZLMcLLlCCmAOgkCghHc0t6FYU)

  

Generating the Key file and copy

near generate-key furla.shardnet.near

    cp ~/.near-credentials/shardnet/YOUR_WALLET.json ~/.near/validator_key.json

![](https://lh5.googleusercontent.com/6w3-IwsSV3wgArpjFhbvkVdCxfPNAvmS0Tq93KLHLceBFU7drxkd6Q_evc24C6uHgYNSnrAHU4UPZwgHxSHXqm4UTHLhtizvB-3RQu1goWP01zsFpb6H6qTc8q5cdtx9vYXg2F7cupgUchus_2pKjv4)

  

    target/release/neard run

![](https://lh5.googleusercontent.com/um21mPeGmZBO1vvRr2tx1nSp5GIB_xc2mWsuGUd6fnvGJrn29sBWw0DFwG5xYxNob3y0WPnahEFRLM7Lm4uwNsVYoC8_jddbmmvyy_tEfnW3h9Onhd9yp9xFAYwDYrO3CJELnslCyCTr1hv2EXOHOYA)

Creating systemd unit and enable/start

    cat <<'EOF' | sudo tee /etc/systemd/system/neard.service
    
    [Unit]
    
    Description=NEARd Daemon Service
    
    [Service]
    
    Type=simple
    
    User=root
    
    #Group=near
    
    WorkingDirectory=/root/.near
    
    ExecStart=/root/nearcore/target/release/neard run
    
    Restart=on-failure
    
    RestartSec=30
    
    KillSignal=SIGINT
    
    TimeoutStopSec=45
    
    KillMode=mixed
    
    [Install]
    
    WantedBy=multi-user.target
    
      
    
    EOF
    
    sudo systemctl enable neard
    
    sudo systemctl start neard

![](https://lh5.googleusercontent.com/Hh9FfL6EQFGavcaP6GAF5lIFDQvcXCIt-zTIGvrvNlsY7X2GGnHA9RutvN3q3QSY0R1NAU1i4PNhtFnQCAM3GRHJvh1UVqnQuT2RtJHmVjr_iG7M_2-xbdubqP4NKKkuL8XvA6QGfuwWz7S3jYu4_4k)

# Challenge 003

##### Deploy a Staking Pool

  

    sed -i 's/private_key/secret_key/' ~/.near/validator_key.json

  and then deploy new pool

    near call factory.shardnet.near create_staking_pool '{"staking_pool_id": "furla", "owner_id": "furla.shardnet.near", "stake_public_key": "ed25519:HGZAKsvNbVy8612SZWhNYXR3eUMZLQsT5fuBZ6XmYdf6", "reward_fee_fraction": {"numerator": 5, "denominator": 100}, "code_hash":"DD428g9eqLL8fWUxv8QSpVFzyHi1Qd16P8ephYCTmMSZ"}' --accountId="furla.shardnet.near" --amount=30 --gas=300000000000000

  

![](https://lh4.googleusercontent.com/rUIIPDobKPiPvMGFe7ZJbeUP_VmMlxITp9RdqEGb4cchyoNO8v1H39iZQGorbGkz82P-qD4MYRlo93YTLLPkcVvGTwzeBlBrxDe3tuWMkOEJ0WLPrkUguFk7pTyE1DqSslVZQm7YkcSxP_lLXbWh6HA)

##### Deposit and Stake NEAR


    near call furla.factory.shardnet.near deposit_and_stake --amount 10 --accountId.shardnet.near --gas=300000000000000

  

![](https://lh5.googleusercontent.com/ErrCYzxi4VWXv-dW96rlvsVdbDib7wDiDlh3VyVy3-lTDN-g_D-UPHDde0KKVYBr7GSVUNz55c0dt1G0mvVFUggR3UxF4SDPxTLvfeOKJU-ltkU4Zngv8zlfiYDgRJkjoExWzXtxZlUn1ysS-xOn82Y)
**Ping**

    near call furla.factory.shardnet.near ping '{}' --accountId furla.shardnet.near --gas=300000000000000

  
  

![](https://lh5.googleusercontent.com/l7kz6pyHVa3zGnX03K6ieIhp-pkAWYQiiOBkllh2pIYTbEj-Wir_LMkAe1IX_JM2r2K3zdzRmmML5dI2SsslDDRMULaLOamFLQvZG_2IsUnTqoec_KZFSd3EQ2WYbgVUamYSSHzQDCRSxw-dZ9j7tkA)

  

# Challenge 004

**log files**

check in dir ~/.nearup/logs with color

    apt install ccze jq curl -y
    journalctl -n 100 -f -u neard | ccze -A

    curl -s http://127.0.0.1:3030/status | jq .version

![](https://lh5.googleusercontent.com/ApTnaaKGWi50Jz0o8LbQUNUcGs8NSiA_MKty4wMtGYENnurXu45rmy2UdEADaMETrPshjkpGLDCev7n-HDtoJteeNneEM57-FIRO62fJOvv6KZloibwyKZoTUZUMFY3ErZrDBqHiAHyttKihhsfeleo)

  

# Challenge 006

**Make directory**

    mkdir -p ~/scripts
    mkdir -p ~/logs
    cat <<'EOF' | sudo tee /root/scripts/ping.sh 
    #!/bin/sh

**Ping call to renew Proposal added to crontab**
  

    export NEAR_ENV=shardnet
    
    export LOGS=/root/logs
    
    export POOLID=furla
    
    export ACCOUNTID=furla
    
      
    
    echo "---" >> $LOGS/all.log
    
    date >> $LOGS/all.log
    
    near call $POOLID.factory.shardnet.near ping '{}' --accountId $ACCOUNTID.shardnet.near --gas=300000000000000 >> $LOGS/all.log
    
    near proposals | grep $POOLID >> $LOGS/all.log
    
    near validators current | grep $POOLID >> $LOGS/all.log
    
    near validators next | grep $POOLID >> $LOGS/all.log
    
      
    
    EOF
    
      
      
    
    chmod +x /root/scripts/ping.sh
    
    crontab -e
    
    0 */1 * * * sh /root/scripts/ping.sh
    
    cat /root/logs/all.log

![](https://lh3.googleusercontent.com/B1-w5ob42ZOdMc8TFTVr7xf_8Qac_AoqgHQSeJ27RzVgZf1WAaV7w1Jy27PsNysvwW56_rKmmTIO--oOzCn_MzDq6wONbPRU2TVL2yhcVnXK71mp05x5Bj36XPb-2Nk9rAilRVFf-WOqNzAcE0lcjHY)

**I guess you got it right with my instructions** ☺


