### Introduction to Smart Contracts
#### Get ready to learn the basics of Solidity
Welcome to our Solidity Course! We will be exploring basic concepts of Solidity and Smart Contracts which will give you enough knowledge to create your own smart contracts and build your own dapps!

#### Where do we begin? Let's explore what Smart Contracts are.
Let us begin with the most basic example. It is fine if you do not understand everything right now, we will go into more detail later.




### The Ethereum Virtual Machine
#### Overview
The Ethereum Virtual Machine or EVM is the runtime environment for smart contracts in Ethereum. It is not only sandboxed but actually completely isolated, which means that code running inside the EVM has no access to network, filesystem or other processes. Smart contracts even have limited access to other smart contracts.

#### Accounts
There are two kinds of accounts in Ethereum which share the same address space: `External accounts` that are controlled by public-private key pairs (i.e. humans) and `contract accounts` which are controlled by the code stored together with the account.

The address of an external account is determined from the public key while the address of a contract is determined at the time the contract is created (it is derived from the creator address and the number of transactions sent from that address, the so-called “nonce”).

Regardless of whether or not the account stores code, the two types are treated equally by the EVM.

Every account has a persistent key-value store mapping 256-bit words to 256-bit words called `storage`.

Furthermore, every account has a `balance` in Ether (in “Wei” to be exact) which can be modified by sending transactions that include Ether.
