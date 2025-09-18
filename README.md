# Votexis: Decentralized Governance Framework

## Overview

Votexis is a governance framework enabling token holders to propose, vote, and execute changes to protocol parameters. It supports on-chain proposals, delegation, voting power snapshots, and execution of approved tasks.

## Features

* Proposal creation with deposits and thresholds
* Configurable governance parameters through system settings
* Categories for proposals: parameter, upgrade, fund, text
* Voting with support, opposition, and abstention tracking
* Delegation of voting power to another principal
* Proposal lifecycle: draft, active, passed, rejected, executed, canceled
* Execution delay before enacting passed proposals
* Task system for parameter updates, fund transfers, and contract calls
* Transparent vote records and proposal status queries

## Data Structures

* **system-parameters**: Protocol parameters with values, types, and descriptions
* **governance-proposals**: Proposals with metadata, lifecycle, and thresholds
* **proposal-tasks**: Actions tied to proposals for execution upon approval
* **vote-records**: Records of votes with choice, power, and optional comments
* **voting-delegations**: Delegation of voting rights to another address

## Key Functions

* `initialize-parameters`: Set default governance parameters
* `create-proposal`: Create a governance proposal
* `add-proposal-task`: Add an action to a proposal
* `activate-proposal`: Move a proposal from draft to active
* `cast-vote`: Cast or update a vote on a proposal
* `delegate-votes`: Delegate voting power to another address
* `remove-delegation`: Remove voting delegation
* `finalize-proposal`: Determine outcome after voting ends
* `execute-proposal`: Execute actions for passed proposals
* `cancel-proposal`: Cancel a proposal before voting starts
* `set-parameter`: Update system parameters via governance

## Read-Only Functions

* `get-proposal`: Retrieve proposal details
* `get-parameter`: Retrieve a parameter’s value
* `get-vote`: Retrieve a specific vote record
* `check-proposal-status`: Check current status of a proposal
* `get-proposal-task`: Retrieve details of a proposal action

## Governance Parameters

* Voting delay
* Voting period
* Execution delay
* Minimum proposal threshold
* Quorum threshold
* Simple and super-majority thresholds
* Treasury address
* Governance token address
* Total token supply

## Error Handling

* Invalid proposal types
* Unauthorized actions
* Insufficient tokens for proposal creation
* Invalid vote choices
* Proposal not found or invalid state
* Execution or finalization errors
