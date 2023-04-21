## Project Description

In this onchain voting system project, we chose to apply ERC721 as the governance token standard. The governance model is quite simple, that anyone with the corresponding type of token can vote through this system where three choices of voting are provided: for, against, and abstain. When the votes are cast, the system will count the number of each option and if the number of "for" outweighs that of "against" the voting will succeed.

## Project Execution

We compiled a contract namely VotingToken.sol to track on the individual votes for a governance on-chain as well as giving to power to delegate a vote to a trusted third-party. With this contract the holders of tokens will have the ability to burn them and administrator of this project can emit or mint tokens. Besides, token with a flexible access control where each action within the DAO requires a separate role, which can be granted to several authorized accounts.

In terms of tests, we wrote two tests (containing a few sub-tests each) towards the functionalities:

- VotingToken: in this script we tested the initial state of the system, the administrator and the minter should be set as the contract owner in default. The minter should be able to mint tokens as well. Meanwhile, the type of the token should also be confirmed (in this case we name it as DTK, standing for Dauphine DAO).
- GovernanceLogic: In this test we set up two test accounts, one as a proposer and the other as a non-proposer. We deployed a new GovernanceLogic contract with the voting token contract's address as the constructor argument and tested the initialization of the contract.
