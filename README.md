# Lottery Smart Contract

## Description

This is a simple Ethereum smart contract written in Solidity that implements a lottery game. Users can participate by sending a small amount of Ether, and a random winner is selected by the manager. The manager is the account that deployed the contract.

## Smart Contract Details

- **Manager**: The `manager` is the Ethereum address of the account that deployed the contract. The manager is responsible for starting the lottery and selecting the winner.

- **Candidates**: `candidates` is an array of payable addresses. Users participate in the lottery by sending a small amount of Ether (0.000001 Ether) to the contract's `receive` function, and their address is added to the `candidates` array.

- **Winner**: The `winner` is the address of the lottery winner. When the manager calls the `pickwinner` function, a random candidate is selected as the winner, and the contract transfers the contract's balance to the winner.

## Usage

To use this lottery contract:

1. Deploy the contract to the Ethereum network, and you will become the `manager`.

2. Participants can send 0.000001 Ether to the contract's address using their Ethereum wallet to join the lottery.

3. Once there are at least two participants, the `manager` can call the `pickwinner` function to select a random winner and transfer the prize money to their address.

4. The `manager` can check the contract's balance using the `getbal` function.

## Contract Rules

- Only the `manager` can pick a winner.

- Participants must send exactly 0.000001 Ether to participate.

- A winner can only be picked when there are at least two participants.

## License

This smart contract is provided under the GPL-3.0 license.

## Note

This is a simple example for educational purposes and should not be used for real-world lotteries or with significant amounts of Ether. Proper security and auditing are essential for production-level smart contracts.

I am still a rookie so I can't create a full fledged web app of this code, hence this code can only be executed in Remix IDE. Thus copy-paste the code and run it in the IDE itself.
