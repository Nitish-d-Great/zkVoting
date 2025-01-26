# ZeroKnowledgeVoting

## Introduction
ZeroKnowledgeVoting is a demonstration application that implements a zero-knowledge voting system utilizing zk-SNARKs. It enables voters to cast their votes anonymously while maintaining the integrity of the voting process. The results are updated in real-time - ensuring enhanced trust and transparency.

### Hackathon Alignment

This project aligns with the Hackathon’s objectives by:

- Leveraging : It uses  ’s Groth16 verifier on the BN-128 curve to validate zero-knowledge proofs.
- Promoting Decentralization : Demonstrates a real-world use case of decentralized proof verification for secure and anonymous voting.
- Innovative Application : Showcases how ZKPs can enhance trust, privacy, and transparency in democratic processes.



## Setup Instructions

### Prerequisites
- Ensure latest version of [Node.js](https://nodejs.org/) is installed. The demo has been tested with **Node.js v23.3.0**.
- You need wallets funded with:
  - **ACME tokens** for   operations. [ You may use Talisman Wallet for the same ]
  - **Sepolia ETH** for Ethereum transactions. [ MetaMask wallet turns out great for this ]

This process submits a transaction to the App Contract, including the necessary attestation details obtained from   (such as the attestation ID and Merkle path). Upon successful submission and validation, the App Contract confirms and acknowledges that your vote has been casted.

## Usage
- **Voting:** Enter your account address (from `voterRegistry.json`) and choose a candidate to cast your vote.
- **Results:** View the real-time voting results on the results page.


### Notes
- Ensure your wallets are sufficiently funded before running the application.
- For more information, refer to the source code or contact the repository owner.

## Technical Architecture


1. **App**:

   - The Node.js backend handles proof generation, verification, and interaction with the blockchain.
   - Provides APIs for vote submission and results display.

2. **Frontend**:

   - Web-based UI built using HTML, CSS and JavaScript for casting votes and viewing results.

3. **zk-SNARK Circuit**:

   - Written in `circom`, the circuit enforces rules such as verifying Merkle paths, vote commitments, and nullifiers.
   - Uses `groth16` as the proving system.

4. **zkVote Smart Contract**:

   - A Solidity contract deployed on the Ethereum blockchain.
   - Integrates with the   platform for off-chain proof verification and ensures rules like no double voting.


## For any more information, contact the owner of the repository. Your views on this project are welcome.

## License
This project is licensed under the MIT License.
