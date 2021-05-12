# XEMXLink

To Host your own node, follow these steps.

Download nodejs 

curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -

apt-get install -y nodejs

add-apt-repository -y ppa:ethereum/ethereum

apt-get update

apt-get install ethereum

Use the genesis.json file provided.

geth init gensis.json

Firewall configurations

ufw enable

Allow UDP and TCP traffic on port 30303

ufw allow 30303/tcp

ufw allow 30303/udp

Start Blockchain

Act as a miner

geth --networkid 1934567 --nat extip:<SERVER_IP> --mine --nodiscover

Only RPC node

geth --networkid 1934567 --nat extip:<SERVER_IP> --nodiscover

Add Peers

geth attach

admin.addPeer("enode://6919ee41d02fc2bc0e39527adeef95c285b2f53ae6b7170c8db37e4daf9368dbec3c32fd872d77f70bc8ae581c868069a72857be2325d7d0a752a72c493683ff@138.197.65.143:59684")

admin.addPeer("enode://d6171439e72e3d257b3ab66a8f772a25355704f2ce1a6e8b9645b5f901dd1c36b8aef78a60124e1d0d8ba64bd5927a1cb8e82d12de599171526a1cdba1233f5e@138.197.15.247:30303?discport=0")

