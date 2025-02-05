---
title: Paying for Gas in Tokens
description: How to pay Celo gas fees using whitelisted ERC20 tokens.
---
# Paying for Gas in Tokens

How to pay Celo gas fees using whitelisted ERC20 tokens.

___

## Transaction Fees

As in Ethereum, transaction fees play a critical role in the Celo protocol as a safeguard against denial-of-service attacks. In order to simplify the process of sending funds, these fees can be paid in ERC20 tokens, and not just the native token of the protocol, CELO. This means that a user sending Celo Dollars to friends or family will be able to pay their transaction fee out of their Celo Dollar balance, and do not need to hold a separate balance of CELO in order to make transactions.

## Fee Currency Field

The protocol maintains a governable whitelist of smart contract addresses which can be used to pay for transaction fees. These smart contracts implement an extension of the ERC20 interface, with additional functions that allow the protocol to debit and credit transaction fees. When creating a transaction, users can specify the address of the currency they would like to use to pay for gas via the `feeCurrency` field. Leaving this field empty will result in the native currency, CELO, being used. Note that transactions that specify non-CELO gas currencies will cost approximately 50k additional gas.
