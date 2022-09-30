# assignment-2
- Title

We have two files AITU_Nurislam_ERC20.sol and AITU_Nurislam_BEP20.sol in the contracts folder. In these files I tried to write a smart contract in ERC20 and BEP20 standard with some functionality, like mint, burn, transfer and delegated transfer.

- Usage

Here I will describe the usage of the second file because the syntax is the same in both standards.
![image](https://user-images.githubusercontent.com/80254372/193319125-1a973b45-3faf-4294-8c3c-ebadfc14f265.png)

The first thing is our variables, the collection "balances" - stores the balance of addresses. 
collection "allowance" - stores allowance from someone to someone.
"totalSupply" - stores the total supply.
"name" - the name of the token.
"symbol" - the symbol of the token.
"decimals" - stores the number of decimals used to get its user representation.

Events for transaction and allowance:

![image](https://user-images.githubusercontent.com/80254372/193320434-098136b7-75d5-4dff-b09c-08592a5ba4c2.png)

Constructor in which the balance of the owner is transferred to "totalSupply":

![image](https://user-images.githubusercontent.com/80254372/193320654-d4406af1-2364-4d02-a9e2-3634c1bb877b.png)

balanceOf(address owner) - you can find the balance by specifying the address of the owner:

![image](https://user-images.githubusercontent.com/80254372/193320828-8f67e2d4-fae3-464f-810d-848b2b0d2c00.png)

transfer(address to, uint value) - to send tokens from the owner to a specific recipient. There is also a require to stop the transfer if the amount of tokens from the owner is not enough:

![image](https://user-images.githubusercontent.com/80254372/193321224-e057a253-3680-4428-a176-ef1d7ca7a80b.png)

transferFrom(address from, address to, uint value) - to perform delegated transmissions. Also here is a require from the previous function and a second one to check the allowance:

![image](https://user-images.githubusercontent.com/80254372/193321480-4afce5d6-f779-4a81-bf60-4e57b7d8e197.png)

approve(address spender, uint value) - to set the allowance for the address:

![image](https://user-images.githubusercontent.com/80254372/193322213-3cf25949-8b01-4140-8a2e-0ee8003651d3.png)


