# BSC-stream-contract

<a href="https://ibb.co/Y3s5Lz4"><img src="https://i.ibb.co/56HQRNX/download-1.png" alt="download-1" border="0"></a>

The Main contract is named "BSC_Stream.sol"

The BSC-Stream Contract Can be summed up in Five Functions 

### 1. Create Stream
   The create stream function transfers the tokens into the BSC-Stream smart contract, stamping the rules of the stream into the blockchain. As soon as the clock hits the start time of the stream, a little bit of money starts getting "transferred" from the sender to the recipient once every second.‌
  The Function parameters are 

- msg.sender : The address which shall fund the stream, and pay the recipient in real-time.
- recipient : The address towards which the money shall be streamed.
- deposit : The amount of money to be streamed, in units of the streaming currency.
- tokenAddress : The address of the ERC-20 token to use as streaming currency.
- startTime : The unix timestamp for when the stream starts, in seconds.
- stopTime : The unix timestamp for when the stream stops, in seconds.
- RETURN : The stream's id as an unsigned integer on success, reverts on error.

<a href="https://ibb.co/vP0LKP7"><img src="https://i.ibb.co/sw8sMw0/BSC-Stream.png" alt="BSC-Stream" border="0"></a><br />
  
### 2. Withdraw From Stream
   The withdraw from stream function transfers an amount of money to the recipient's address. The amount must be less than or equal to the available balance. This function can only be called by the sender or the recipient of the stream, not any third-party.

- streamId : The id of the stream to withdraw money from.
- amount : The amount of money to withdraw.
- RETURN : True on success, false on error.
  
### 3. Cancel Stream
   The cancel stream function revokes a previously created stream and returns the money back to the sender and/or the recipient. If the clock did not hit the start time, all the money is returned to the sender. If the clock did go past the start time, but not past the stop time, the sender and the recipient both get a pro-rata amount. Finally, if the clock went past the stop time, all the money goes the recipient. This function can be called only by the sender.

- streamId : The id of the stream to cancel.
- RETURN : True on success, false on error.

### 4. Get Stream
   The get stream function returns all properties for the provided stream id. All information about the stream is returned back or called

- streamId : The id of the stream to query.
- RETURN : info such as sender, recipient, tokenAddress, startTime, stopTime, remainingBalance, ratePerSecond 

### 5. Balance Of
The balance of function returns the real-time balance for an address, with respect to a specific stream.

- streamId : The id of the stream for which to query the balance.
- who : The address for which to query the balance.
- RETURN : The available balance in units of the streaming currency.

## How to Run

The Network Details and Steps to Run this contract

- Go to Metamask
- Select "Add a New Network"
- Fill in with the following information

<a href=""><img src="https://lh5.googleusercontent.com/wRHX351ldc2PWT1wXE6U1NYyUkaEmVHVoA0Ex4LKz51prqRgwJcBCs2DhL0lQ3PVmE7Sv2dE02ReXcHlXNaf0lczFZtFl5htOtAzUYkDzu5eySe7y4wpcMaCzY6GaHv6NCXM1qZQ" alt="download" border="0"></a>
 <br />

#### Testnet

RPC URLs ( Select Any One)   <br />
https://data-seed-prebsc-1-s1.binance.org:8545/ <br />
https://data-seed-prebsc-2-s1.binance.org:8545/ <br />
https://data-seed-prebsc-1-s2.binance.org:8545/  <br />
https://data-seed-prebsc-2-s2.binance.org:8545/  <br />
https://data-seed-prebsc-1-s3.binance.org:8545/  <br />
https://data-seed-prebsc-2-s3.binance.org:8545/  <br />
ChainID: 0x61, 97 in decimal (if 97 doesn’t work, try 0x61) <br />
Symbol: BNB <br />
Block Explorer: https://testnet.bscscan.com   <br />
#### Mainnet <br />

RPC URLs ( Select Any One)  <br />

https://bsc-dataseed.binance.org/  <br />
https://bsc-dataseed1.defibit.io/   <br />
https://bsc-dataseed1.ninicoin.io/    <br />


ChainID: 0x38, 56 in decimal (if 56 doesn’t work, try 0x38)  <br />
Symbol: BNB  <br />
Block Explorer: https://bscscan.com  <br />

NOTE: We are currently using the BSC TestNetwork for the test phase of our contract. hence fill the info likewise.  <br />

NOTE: Currently active deployed contract on the BSC TestNetwork at Address: <a href="https://testnet.bscscan.com/address/0x8582f3B4CFd18b8FA66A352AE25F6D2DC2A359e3"> 0x8582f3B4CFd18b8FA66A352AE25F6D2DC2A359e3 </a>  <br />

      

