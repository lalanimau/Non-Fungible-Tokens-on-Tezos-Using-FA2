# Non-Fungible-Tokens-on-Tezos-Using-FA2

### Requirement:
Node.js

Docker

### Commands to run 

`npm install -g https://github.com/tqtezos/nft-tutorial.git`

`tznft bootstrap`

minting : `tznft mint <owner_alias> --tokens <token_meta_list>`

tznft mint bob --tokens '0, T1, My Token One' '1, T2, My Token Two'

inspecting : `tznft show-meta --nft Token Deployed Address Here --signer bob --tokens 0 1`

Token Balance: `tznft show-balance --nft <Token Deployed Address Here> --signer bob --owner bob --tokens 0 1`


Transfering Token: `tznft transfer --nft <Token Deployed Address Here> --signer bob --batch 'bob, alice, 0' 'bob, alice, 1'`


