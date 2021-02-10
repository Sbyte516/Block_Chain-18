Net1/Net2
./puppeth

seed.json

Neywork: seed ID: 441
The Network is an additional way to tell chains apart and is required when signing transactions.

password:password

Private Keys and Public Keys terms are used in encryption and decryption. These keys are used to encrypt/decrypt sensitive information.

The private key is used to both encrypt and decrypt the data. This key is shared between the sender and receiver of the encrypted sensitive information. 
The private key is also called symmetric being common for both parties. Private key cryptography is faster than public-key cryptography mechanism.
The private key is kept secret and not public to anyone apart from the sender and receiver.

The public key isused to encrypt data.
The public key mechanism is called asymmetric being two keys for different purposes.
The public key can be used by anyone.

Data encrypted with the public key can only be decrypted with the private key, and data encrypted with the private key can only be decrypted with the public key

private key: #####
Create Nodes
./geth account new --datadir Net1

Public address of the key:   0x2Baf73D8293B37bBbDe0D4C286f4d0D890F45817
Path of the secret key file: Net1\keystore\UTC--2021-02-10T02-45-07.517252700Z--2baf73d8293b37bbbde0d4c286f4d0d890f45817

./geth account new --datadir Net2

Public address of the key:   0x48fa2149058aB88219e2185F9619D933FcBeD047
Path of the secret key file: Net2\keystore\UTC--2021-02-10T02-46-17.319281000Z--48fa2149058ab88219e2185f9619d933fcbed047


Start Node 1
./geth --allow-insecure-unlock --datadir node1 --unlock "Node 1 public address" --mine --rpc
enode://6485277ddb7a7391732fd68a1f02705765e54805a00015d45e69f4c01d037a5f8d1a85d21a2ec9978d7be8133b197601a967b6ec81dbc0a807a8cd326e66ab7e@127.0.0.1:30303

Start Node 2
./geth --allow-insecure-unlock --datadir node2 --unlock "Node 2 public address" –-mine --port 30304 --bootnodes "enode://from Node 1" --ipcdisable
The only issue is you might not need the "--ipcdisable" at the end of Node 2


password: password

Initialize Node
./geth init seed.json --datadir Net1
./geth init seed.json --datadir Net2

Testnet(ETH) (m/44'/1'/0'/0)
Address #2: 0xF7587Aa5918aEE4E1ab9596943F50dF537a07389 (Pre-fund)
            0xF7587Aa5918aEE4E1ab9596943F50dF537a07389

Begin mining 

./geth --allow-insecure-unlock --datadir Net1 --unlock "2Baf73D8293B37bBbDe0D4C286f4d0D890F45817" --mine --rpc




./geth --allow-insecure-unlock --datadir Net2 --unlock "48fa2149058aB88219e2185F9619D933FcBeD047" --mine --port 30304 --bootnodes "enode://c0feda842bb152e20fa2604b1e9ee7db2c97a50ceaa6f2b09bafae4474d9d5ecdc00d04eeed44e126abb33221ac90bae809635008bad565e39fcba730201b9ca@127.0.0.1:30303
" --ipcdisable

enode://c0feda842bb152e20fa2604b1e9ee7db2c97a50ceaa6f2b09bafae4474d9d5ecdc00d04eeed44e126abb33221ac90bae809635008bad565e39fcba730201b9ca@127.0.0.1:30303


Block time is the length of time it takes to create a new block or file in a cryptocurrency chain.
A block is verified by bitcoin miners, who compete against each other to solve a mathematical problem that is attached to the block.
The successful bitcoin miner is rewarded in cryptocurrency.

A block is a file that records a number of the most recent cryptocurrency transactions.
Each block contains a reference to the block that preceded it. (That's why it is theoretically impossible to alter cryptocurrency.)
Cryptocurrency "miners" race against each other to solve a mathematical puzzle embedded in the file. The winner is paid in cryptocurrency.
The solution to the puzzle triggers the currency's acceptance as a new block on the blockchain. The block has been validated. (The miner is rewarded with cryptocurrency.)


Mneumonic
term destroy elevator measure surge alone refuse length payment initial desk sibling

*rm -Rf 
