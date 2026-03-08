# assignment01bca - Simple Blockchain in Go

A simplified blockchain implementation in Go that demonstrates block structure, hash linking, immutability, tamper detection, and chain verification logic.

## Features

- Block creation with SHA-256 hashing
- Chain verification to detect tampering
- Genesis block with personalized roll number data
- Tamper demonstration showing how changing a block breaks the chain

## Project Structure

```
assignment01bca_1557/
├── main.go                        # Entry point - creates blocks and demonstrates tampering
├── go.mod                         # Go module file
└── assignment01bca/
    ├── assignment01bca.go         # Blockchain package with all core functions
    └── go.mod                     # Package module file
```

## Functions

- `NewBlock(transaction, nonce, previousHash)` - Creates a new block and adds it to the chain
- `ListBlocks()` - Prints all blocks with their details
- `ChangeBlock(index, newTransaction)` - Modifies a block's transaction (simulates tampering)
- `VerifyChain()` - Validates the entire blockchain integrity
- `CalculateHash(stringToHash)` - Generates SHA-256 hash from the given string

## How to Run

1. Make sure Go is installed on your system
2. Clone this repository
3. Navigate to the project folder
4. Run the following commands:

```bash
go mod tidy
go run main.go
```

## Expected Output

- Blockchain prints 4 blocks (Genesis + 3 transactions)
- First verification confirms the chain is **valid**
- Block 1 is tampered with
- Second verification detects tampering and reports the chain as **invalid**

## Course

Blockchain and Cryptocurrency - Assignment 01
