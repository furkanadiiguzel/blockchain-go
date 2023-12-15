# Simple Blockchain Implementation in Go

This Go project demonstrates a basic implementation of a blockchain. It includes a simple blockchain structure, blocks with proof-of-work (PoW), and functionalities to add blocks to the chain. The project also showcases the validation of the blockchain.

## Overview

This blockchain implementation is written in Go and includes the following components:

- **Block Structure:** Represents a block in the blockchain, containing data, a hash, the previous hash, a timestamp, and a proof-of-work value.

- **Blockchain Structure:** Consists of a genesis block and a chain of subsequent blocks. It includes methods to create a blockchain, add blocks with transaction data, and validate the integrity of the blockchain.

## How to Use

1. **Create a Blockchain Instance:**
   ```go
   blockchain := CreateBlockchain(2)
   ```

2. **Add Blocks to the Blockchain:**
   ```go
   blockchain.addBlock("Furkan", "Adıgüzel", 5)
   blockchain.addBlock("Nakruf", "Adıgüzel", 2)
   ```

3. **Validate the Blockchain:**
   ```go
   isValid := blockchain.isValid()
   fmt.Println("Is Blockchain Valid? ", isValid)
   ```

4. **Explore Blockchain Information:**
   ```go
   fmt.Println("Genesis Block: ", blockchain.genesisBlock)
   fmt.Println("Blockchain Length: ", len(blockchain.chain))
   fmt.Println("Blockchain Difficulty: ", blockchain.difficulty)
   fmt.Println("Last Block: ", blockchain.chain[len(blockchain.chain)-1])
   ```

5. **Retrieve Block Data:**
   ```go
   fmt.Println("Last Block Data: ", blockchain.chain[len(blockchain.chain)-1].data)
   ```

6. **Example Output:**
   ```go
   Is Blockchain Valid? true
   Genesis Block: {0  2023-12-15 17:04:47.8856924 +0000 UTC 0}
   Blockchain Length: 3
   Blockchain Difficulty: 2
   Last Block: {map[from:Furkan to:Adıgüzel amount:5] 2 8a2d1f3de80b377916a558ff63a99a05e7089538a758ea497c9cd4f1f02a7b56 00b470abdb0ed5a9e5d8305e61154b8037bfef774ab40fa9631768577cd9044e 2023-12-15 17:04:47.9056924 +0000 UTC 3}
   ```

## Dependencies

This project relies on the standard Go libraries and does not require any external dependencies.

## Acknowledgments

This blockchain implementation serves as a starting point for understanding the fundamentals of blockchain technology. Developers are encouraged to explore, modify, and extend the codebase to enhance their understanding of blockchain concepts in a practical setting.

Feel free to experiment, customize, and delve into the code to gain insights into the inner workings of a basic blockchain.
