### Introduction to Smart Contracts
#### Get ready to learn the basics of Solidity
Welcome to our Solidity Course! We will be exploring basic concepts of Solidity and Smart Contracts which will give you enough knowledge to create your own smart contracts and build your own dapps!

#### Where do we begin? Let's explore what Smart Contracts are.
Let us begin with the most basic example. It is fine if you do not understand everything right now, we will go into more detail later.

#### Storage
 ```
 pragma solidity ^0.4.0;

contract SimpleStorage {
    uint storedData;

    function set(uint x) public {
        storedData = x;
    }

    function get() public view returns (uint) {
        return storedData;
    }
}
```
The first line simply tells that the source code is written for Solidity version 0.4.0 or anything newer that does not break functionality (up to, but not including, version 0.5.0). This is to ensure that the contract does not suddenly behave differently with a new compiler version. The keyword `pragma` is called that way because, in general, pragmas are instructions for the compiler about how to treat the source code.

A contract in the sense of Solidity is a collection of code (its functions) and data (its state) that resides at a specific address on the Ethereum blockchain. The line `uint storedData;` declares a state variable called `storedData` of type `uint` (unsigned integer of 256 bits). You can think of it as a single slot in a database that can be queried and altered by calling functions of the code that manages the database. In the case of Ethereum, this is always the owning contract. And in this case, the functions `set` and `get` can be used to modify or retrieve the value of the variable.

To access a state variable, you do not need the prefix `this.` as is common in other languages.

This contract does not do much yet (due to the infrastructure built by Ethereum) apart from allowing anyone to store a single number that is accessible by anyone in the world without a (feasible) way to prevent you from publishing this number. Of course, anyone could just call `set` again with a different value and overwrite your number, but the number will still be stored in the history of the blockchain. Later, we will see how you can impose access restrictions so that only you can alter the number.

 #### here is another subtitle
 and some text below it
