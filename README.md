# P2P Loan System

## Project Title
P2P Loan System

## Project Description
A decentralized peer-to-peer lending platform built on the Stellar blockchain using Soroban smart contracts. This system enables direct lending between individuals without traditional financial intermediaries, providing a transparent, efficient, and secure environment for borrowers to request loans and lenders to fund them. The platform records all loan activities on the blockchain, ensuring immutable record-keeping and contractual enforcement through code.

## Project Vision
Our vision is to democratize lending by creating a global, borderless marketplace where individuals can engage in peer-to-peer financial transactions without the need for traditional banking institutions. By leveraging blockchain technology, we aim to:

1. Reduce the entry barriers to accessing credit, particularly for the underbanked population
2. Eliminate unnecessary intermediaries and their associated costs
3. Provide transparent and immutable loan agreements
4. Create a trustless environment where contractual obligations are enforced through code
5. Enable cross-border lending without the friction of traditional international transfers

The P2P Loan System strives to be more than just a lending platform; it aims to be a catalyst for financial inclusion and empowerment by connecting lenders with excess capital to borrowers with genuine needs, all while ensuring fair terms and secure transactions.

## Key Features

| Feature | Description |
|---------|------------|
| **Loan Requests** | Borrowers can create loan requests specifying amount, interest rate, term, and purpose |
| **Direct Funding** | Lenders can browse and fund loan requests directly, with funds held in escrow until terms are met |
| **Smart Contract Enforcement** | Loan terms, repayments, and defaults are automatically enforced by the smart contract |
| **Transparent Records** | All loan activities are recorded on the blockchain and publicly verifiable |
| **Reputation System** | Users build verifiable on-chain credit history through their lending and borrowing activities |
| **Automated Repayments** | The system supports scheduled repayments with automatic tracking and notifications |
| **Default Management** | Clear processes for handling defaults with minimal friction and maximum transparency |
| **Platform Analytics** | Real-time statistics on total loans, active loans, repayment rates, and platform volume |

## Technical Implementation

The smart contract is implemented using Soroban SDK, which provides a robust framework for developing financial applications on the Stellar blockchain. The core components include:

- **Loan Structure**: Stores comprehensive loan details including borrower, lender, amount, terms, and status
- **Status Tracking**: Manages the lifecycle of loans from request through funding, repayment, or default
- **Authentication**: Uses Soroban's authentication system to verify user identity for loan operations
- **Statistics Tracking**: Maintains platform-wide metrics for transparency and analysis

## Contract Functions

1. **request_loan**: Creates a new loan request with specified terms
2. **fund_loan**: Allows a lender to fund an existing loan request
3. **repay_loan**: Enables borrowers to repay their loans
4. **mark_defaulted**: Allows lenders to mark loans as defaulted after the deadline
5. **get_loan**: Retrieves detailed information about a specific loan
6. **get_loan_stats**: Provides platform-wide statistics on lending activities

## Getting Started

### Prerequisites
- Soroban CLI
- Stellar development environment

### Installation
1. Clone the repository
2. Install dependencies
3. Build the smart contract
4. Deploy to the Stellar testnet or mainnet

### Usage Examples
```rust
// Create a loan request
let loan_id = client.request_loan(
    borrower_address,
    10000,           // 100.00 tokens (assuming 2 decimal places)
    500,             // 5.00% interest rate
    30,              // 30-day term
    "Business expansion"
);

// Fund a loan
client.fund_loan(lender_address, loan_id);

// Repay a loan
client.repay_loan(borrower_address, loan_id);
```

## Security Considerations

The contract implements several security measures:
- Authentication requirements for all loan operations
- Prevention of self-funding loans
- Deadline enforcement for defaulted loans
- Clear state management to prevent invalid state transitions

## Future Enhancements

- Collateralized loans
- Variable repayment schedules
- Secondary market for loan trading
- Interest rate algorithms based on credit scores
- Multi-currency support
- Escrow mechanisms for dispute resolution
- Integration with decentralized identity solutions

## Contract Details
Contract Address: CCDNQ3DSX4YMUFZ47QXI5YR3FCJVSUHAN3TFSBPGQRLYT7XFIJTQQLDQ

## License
This project is licensed under the MIT License - see the LICENSE file for details.
