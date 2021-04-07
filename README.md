# Unit-18-Blockchain
Proof of Authority Blockchain Development

# Instructions

### Start the Network
    Initialize the nodes with the genesis' json file.  This step will initilize the nodes for the zbanknet network after 
    the genesis block has been created.  Datadir defines the directory and init will referense the JSON genesis block file. 

    ./geth --datadir nodehw1 init zbanknet/zbanknet.json 
    ./geth --datadir nodehw2 init zbanknet/zbanknet.json 
      
    Bringing your blockchain to life - Run the nodes in separate terminal windows with the commands

    <strong>nodehw1</strong>
    ./geth --datadir nodehw1 --unlock "4d318F0d83e540c0A6Aa53d274828ca11Df442a8" --mine --minerthreads 1
    
    <strong>nodehw2</strong>
    ./geth --datadir nodehw2 --unlock "3B15eA2209ce5025e2fb737d561B675a3c520269" --port 30304 --rpc --bootnodes
    "enode://e7a262503e77ca19b5e087293087ca947d6b7d71453bca4869bd78583e1bc913317526424b1072bf590213b7e057849aa981a84099dc67966ea60b42214b88e5@127.0.0.1:30303"
    --ipcdisable --allow-insecure-unlock

    

    
### Configuration of the Network
    test
    
### MyCrypto Steps
    test
