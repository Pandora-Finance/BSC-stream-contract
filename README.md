# BSC-stream-contract

The BSC-Stream Contract Can be summed up in Five Functions 

### 1. Create Stream
   The create stream function transfers the tokens into the Sablier smart contract, stamping the rules of the stream into the blockchain. As soon as the clock hits the start time of the stream, a little bit of money starts getting "transferred" from the sender to the recipient once every second.‌
  The Function parameters are 

- msg.sender : The address which shall fund the stream, and pay the recipient in real-time.
- recipient : The address towards which the money shall be streamed.
- deposit : The amount of money to be streamed, in units of the streaming currency.
- tokenAddress : The address of the ERC-20 token to use as streaming currency.
- startTime : The unix timestamp for when the stream starts, in seconds.
- stopTime : The unix timestamp for when the stream stops, in seconds.
- RETURN : The stream's id as an unsigned integer on success, reverts on error.
  
