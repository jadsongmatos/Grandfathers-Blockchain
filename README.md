
# Grandfather's Blockchain

## Introduction
Currently blockchains that use proof of work to ensure their integrity rely on massive processing GPUs used to create hashing that starts zeros in front, weighing how to take advantage of this processing was thinking of a blockchain model that uses search algorithms as proof of work.

Briefly explaining how proof of work works in the blockchain, proof of work is one of the ways to ensure that a valid block, since to generate a false block it is necessary to go through proof of work again and so on to the most current block, algorithm chosen as proof of work in most blockchain as bitcon consists and find hash starting with quantity specify zeros in as, for example in 2021 difficulty of bitcoin blocks was in 19 zeros.

Thinking of a way to make a proof of work process generate something using a search algorithm, which would work similar to a compression system looking for equal parts in the files and creating a link between them, thus generating a new block without duplicated parts, thus reducing the size of the blockchain.
## Possibilities
Avo's blockchain would allow to create a central backup system where files can be saved within blocks and in a distributed and secure way, allows companies to create service to access this file remotely, allows people to earn coins in exchange to find equal parts within blockchain .

### Implementation
The objective is to discuss what would be the most efficient way to implement avo's blockchain idea

### File creation
This would be an example of a structure for the files, inspired by the .torrent file format


```yaml
   {
	"path": "/img/pato.png",
	"data": "2020-2-5T10:41:10",
	"uuid": "0054-asd46-asd",
	"pieces": ["as54fd5q234", "vq942z5t23d", "4d5adas2fte"],
	"new_pieces": {
		"4d5adas2fte": "0110110011",
		"vq942z5t23d": "00011110"
	}
} 
```
#### About the fields

 - Path
	 - It would be a field where there would be an easy-to-read path
 - Data
	 - Recording the creation date of the file for search purposes
 - UUID
	 - An identifier of the user who created the file
 - Pieces
	 - List of hash containing parts of file data
 - New Pieces
	 - Key-value list containing hash of parts that do not yet exist in the blockchain along with data from that part


## Search algorithm
Not yet defined

## Storage
Blockchain storage can be done differently, but two main ones would be through its own file system with folder and files or using database like mysql, which depends on the user may be more suitable, for example for a user who will not be part of the mining process When the space used is more important then a system other than mysql would be the most ideal, since for someone it will be part of the training process will do a constant search in the binaries of the files have a system as a database would be more ideal.

## Currency
	
### Validation
If block was validated the miner earns amount of coins relative to the amount of equal parts he found.

### Reward for mining
This contract created where those who seek equal parts in the files that are already inside the Blockchain earn rewards, when finding equal parts, the miner sends files with addresses of the same parts, if it is valid in the next block, that duplicate section will be removed to be just a link, quantity of coins generated is relative amount of bytes doubled.

### Warranty system
Thinking of a way to prevent users on the public network from trying to send noise to Blockchain to harm its functioning, the guarantee system requires that the user has a quantity of coins relative to the size of the file, if during the block validation process any equal part is found, it is generated discount and in the next block will be returned the amount of coins relative to the amount of equal parts found.
