# Non-Fungible-Tokens-on-Tezos-Using-FA2

### Requirement:
Node.js

Docker

### Commands to run 

`npm install -g https://github.com/tqtezos/nft-tutorial.git`

`tznft bootstrap`

This is start the Docker SandBox for local chain of Tezos

minting : `tznft mint <owner_alias> --tokens <token_meta_list>`

This is the syntax in which we need to paas the pass the Data in order to create the Token

`tznft mint bob --tokens '0, T1, My Token One' '1, T2, My Token Two'`

Here we are creating 2 Tokens ie.

'0, T1, My Token One' where '0' is the token Id , 'T1' is the symbol of the Token and 'My Token One' is the name of the Token 

'1, T2, My Token Two' where '1' is the token Id , 'T2' is the symbol of the Token and 'My Token Two' is the name of the Token 

Once this command is successfully executed, It will return the token address where it is deployed.

inspecting : `tznft show-meta --nft <Token Deployed Address Here> --signer bob --tokens 0 1`

By this command we can see the details of the NFT.

where --singer means 'alias on behalf of which contract is inspected'

'bob' is one of the alias provided by Tezos by default. (By default Tezos Provide 2 alias/account ie. bob and alice)

--tokens means we need to provide the ID for the Token. (In our case it is 0 and 1)

expected output:

token_id: 0 symbol: T1  name: My Token One  extras: { }

token_id: 1 symbol: T2  name: My Token Two  extras: { }


Token Balance: `tznft show-balance --nft <Token Deployed Address Here> --signer bob --owner bob --tokens 0 1`

This command will return balance for that Token.

expected output:

owner: tz1YPSCGWXwBdTncK2aCctSZAXWvGsGwVJqU token: 0    balance: 1

owner: tz1YPSCGWXwBdTncK2aCctSZAXWvGsGwVJqU token: 1    balance: 1


Transfering Token: `tznft transfer --nft <Token Deployed Address Here> --signer bob --batch 'bob, alice, 0' 'bob, alice, 1'`

This will transfer Tokens from bob to alice


