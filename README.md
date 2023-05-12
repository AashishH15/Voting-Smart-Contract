Voting Smart Contract

This is a simple smart contract written in Solidity language for conducting voting. It allows adding candidates and casting votes for them. The smart contract keeps track of the number of votes each candidate has received and can determine the winner.

Prerequisites
To compile and deploy this smart contract, you need the following:

A Solidity compiler. This contract was written using Solidity version 0.8.0.
An Ethereum client or blockchain to deploy and interact with the smart contract.
Installation
To use this smart contract, follow these steps:

Clone the repository to your local machine.
Install the required dependencies. This contract uses the OpenZeppelin library, which can be installed using npm:
npm install @openzeppelin/contracts

Compile the smart contract using your Solidity compiler.
Deploy the smart contract to your Ethereum client or blockchain.

Usage
Once the smart contract is deployed, you can interact with it using any Ethereum wallet that supports contract interaction.

Adding Candidates
To add a candidate, call the addCandidate function and pass the candidate's name as a parameter. This function can only be called by the contract owner.

Casting Votes
To cast a vote, call the vote function and pass the ID of the candidate you want to vote for as a parameter. Each voter can only vote once.

Determining the Winner
To determine the winner of the election, call the determineWinner function. This function returns the ID and name of the winning candidate. If there is a tie, the function returns 0 as the ID and the string "Tie" as the name.

Ending the Voting
To end the voting and determine the winner, call the endVoting function. This function will call determineWinner internally and emit a winnerEvent event with the ID and name of the winning candidate.

MIT License.
