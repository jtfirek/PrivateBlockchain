# Private Blockchain Application

This my first blockchain development project. I have created a simple blockchain application using node.js. Users can use a rest API to interact with my chain. The application allows users to register stars on my custom blockchain and assing ownership of the star to their wallet address. I thought building a blockchain would be a good way to learn more about their structure.

### Blockchain structure

The block object contains a hash of the block, a timestamp, the current blockchain height, a hash of the previous block and a json body that contains the transaction stored in the block. The blockchain object contains an array of blocks and the height of the chain.

### Details
The application creates a genesis block when we run the application. 
Star information will be in this format.
    The Start information will be formed in this format:
    ```json
        "star": {
            "dec": "68° 52' 56.9",
            "ra": "16h 29m 1.0s",
            "story": "Testing the story 4"
		}
    ```

### Steps to use 


1. The application will create a Genesis Block when we run the application.
2. The user will request the application to send a message to be signed using a Wallet and in this way verify the ownership over the wallet address. The message format will be: `<WALLET_ADRESS>:${new Date().getTime().toString().slice(0,-3)}:starRegistry`;
3. Once the user have the message the user can use a Wallet to sign the message.
4. The user will try to submit the Star object for that it will submit: `wallet address`, `message`, `signature` and the `star` object with the star information.
    The Start information will be formed in this format:
    ```json
        "star": {
            "dec": "68° 52' 56.9",
            "ra": "16h 29m 1.0s",
            "story": "Testing the story 4"
		}
    ```
