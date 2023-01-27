# Blockchain-in-JavaScript

This example creates a simple blockchain with a `Block` and `Blockchain` class. The `Block` class has a constructor that takes an index, timestamp, data, and previous hash, and calculates the hash of the block using the SHA-256 algorithm. The `Blockchain` class has a constructor that creates a genesis block and an array to store the blockchain. The class also has methods to add new blocks, get the latest block, and check if the blockchain is valid by iterating through the chain and checking the hash and previous hash of each block.

#### The prerequisites to run this code are as follows: ####

 1. A computer with a web browser or a server with Node.js installed.
 2. An text editor software to open and edit the script.
 3. Internet connection to run the script

The script uses the `crypto` module that is built-in to Node.js, which provides cryptographic functionality that includes the ability to create hash values using the SHA-256 algorithm.

As this script is written in JavaScript, it can run on the browser as well as on the server using Node.js, but the user will need to run the script in an environment that supports JavaScript.

You can check if Node.js is installed on your computer by running the command `"node -v"` in the command line. If Node.js is not installed, you can download and install it from the official [Node.js website](https://nodejs.org/en/)

You can run the script on browser as well by creating an HTML file which includes this script as a script tag and then open the HTML file in browser.


#### The `Block` class is responsible for creating new blocks that will be added to the blockchain. Each block has the following properties: ####

 - `index`: a unique number that identifies the block in the chain
 - `timestamp`: the date and time the block was created
 - `data`: the data that is stored in the block
 - `reviousHash`: the hash of the previous block in the chain
 - `hash`: the unique hash of the current block, calculated using the SHA-256 algorithm

The class has a constructor that takes four arguments: `index`, `timestamp`, `data`, and `previousHash`. The previousHash argument is optional and defaults to an empty string. The constructor sets the properties of the block based on the arguments and calculates the `hash` property using the `calculateHash()` method, which takes no arguments and returns the SHA-256 hash of the block's index, previous hash, timestamp, and data.

#### The `Blockchain` class is responsible for creating the blockchain and maintaining it. The class has the following properties: ####

 - `chain`: an array that stores the blocks in the blockchain

#### The class has the following methods: ####

 - `createGenesisBlock()`: creates the first block in the blockchain, known as the genesis block.
 - `getLatestBlock()`: returns the latest block in the blockchain.
 - `addBlock(newBlock)`: adds a new block to the blockchain. It sets the previousHash property of the new block to the hash of the latest block, and then calculates the new block's hash property using the calculateHash() method.
 - `isChainValid()`: Iterates through the chain and checks the hash and previous hash of each block. It returns true if the chain is valid else false.

The script also creates an instance of the `Blockchain` class called `coin` and adds two new blocks to it with the `addBlock()` method, and then logs the entire blockchain to the console in a human-readable format. It also logs the result of the `isChainValid()` method, which indicates whether the blockchain is valid or not.

This is just a simple example of how a blockchain can be implemented in JavaScript, and it does not include all the features and security measures that a real blockchain would have. But it can be useful for understanding the basic concepts and structure of a blockchain.


