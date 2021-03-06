# Unit-18-Blockchain
Proof of Authority Blockchain Development for ZBank, a small, innovative bank that is interested in exploring what
blockchain technology can do for them and their customers.

I am setting up a testnet as a proof of concept for blockchain usage at ZBank using the below tools: 

* Puppeth, to generate your genesis block.
* Geth, a command-line tool, to create keys, initialize nodes, and connect the nodes together.
* Proof of Authority algorithm.
* MyCrypto Wallet

# Instructions

### Installing dependencies and environment configuration
* Download and Install MyCrpto to be used key mangaement and crypto wallet - https://download.mycrypto.com/
* Install Go Ethereeum Tools - https://geth.ethereum.org/downloads/

### Start the Network
    Initialize the nodes
    
    Initialize the nodes with the genesis' json file.  This step will initilize the nodes for the zbanknet network after 
    the genesis block has been created.  Datadir defines the directory and init will referense the JSON genesis block file. 

    ./geth --datadir nodehw1 init zbanknet/zbanknet.json 
    ./geth --datadir nodehw2 init zbanknet/zbanknet.json 
      
    Starting the nodes
    
    Run the nodes in separate terminal windows with the commands.  We'll run geth program.
    --datadir
        to specify the directory
    --unlock
        to indicate the address of the node we are unlocking
    --mine
        indicates we want to mine
    --minderthreads
        indicates how many cpu cores to dedicate to mining activity
    --port
        specifies the port for node2 to use
    --rpc
        is a remote call procedure when a computer program causes a procedur to execute in a different address space
    --boodnotes
        you must pass in the enode listed from node1
    --ipcdisable
        disables the IPC-RPC server
    --allow-insecure-unlock 
        allows access to the node with geth via HTTP protocal this is used in MyCrypto Wallet
    
    Start nodehw1
        ./geth --datadir nodehw1 --unlock "4d318F0d83e540c0A6Aa53d274828ca11Df442a8" --mine --minerthreads 1
    
    Start nodehw2
        ./geth --datadir nodehw2 --unlock "3B15eA2209ce5025e2fb737d561B675a3c520269" --port 30304 --rpc --bootnodes
        "enode://e7a262503e77ca19b5e087293087ca947d6b7d71453bca4869bd78583e1bc913317526424b1072bf590213b7e057849aa981a84099dc67966ea60b42214b88e5@127.0.0.1:30303"
         --ipcdisable --allow-insecure-unlock

    
### Configuration of the Network
    Blocktime - 15 seconds
    Chain ID - 1234
    Account Passwords - password / password2 for nodehw1 and nodehw2 respectively.  The same password is used for the json files for these nodes.
    
    Ports:
        nodehw1 - ip=127.0.0.1 udp=30303 tcp=30303
        nodehw2 - ip=127.0.0.1 udp=30304 tcp=30304
        MyCrypto URL - http://127.0.0.1:8545
    
### Reference Screenshots
Network Config
![Screenshot](/zbanknet/Screenshots/config.png)

Init Nodes
![Screenshot](/Images/initnodes.png)

Start Node1
![Screenshot](/Images/startnodehw1.png)

Start Node2
![Screenshot2](/Images/startnodehw2.png)

Confirm Transaction

![Screenshot3](/Images/transconfirm.png)

Broadcast Transaction
![Screenshot4](/Images/transbroadcast.png)

Transaction Status
![Screenshot5](/Images/sendtrans.png)
