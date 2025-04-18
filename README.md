

![1](https://github.com/user-attachments/assets/8d07c141-d9e7-4dca-b26b-1879fd4556dc)


Issues and Bounties details: https://scoutgame.xyz/info/partner-rewards/celo

Contribution guide: https://developing-starfish-03e.notion.site/Superflow-Scout-Game-185cbe8a75dd80bc8dafc5833cb04afe


Superflow is built to solve and ease out the process of Token Generation events and later bridging and deploying liquidity pools of those tokens across multiple chains. 

Usually a normal process for TGE and Post TGE looks something like this:

1. Deploying ERC20 on one chain, for most projects, its Ethereum Mainnet for security and trust.
2. Bridge tokens to multiple chains of interest, for example, Arbitrum, Base, Celo, Unichain, etc., or whichever chain they want their token to be present in the LP pool of that chain, Uniswap on Arbitrum or Aerdrome on Base.
3. Actually creating a liquidity pool of the bridged token and the respective destination chains and providing liquidity in that pool.

   
Superflow is built to automate the above-mentioned disjoint and time-consuming steps with one click. 
With Superflow, you provide the necessary information, like the origin chain, total supply, and other metadata of the token, which all chains they want to bridge their tokens to, and how much of the total supply they want to bridge and put in the LP pool for that chain. 

With all this info collected beforehand, Superflow will do all the actions mentioned above for you, and you'll have the deployment result, like the LP Pool address of each destination chain, etc., as the end result.
All of the steps from token generation to bridging to creating an LP pair and providing liquidity abstracted for you under the hood.

That's Superflow!

## How its made

Superflow is a containerised cli solution that automates all the logic for you. The end result is a docker image that you run by executing a single docker command.

Under the hood the different individual steps are automated with JS and Go scripts.

- Token generation happen through a JS script.
- Bridging the token after creation is done using hyperlane warp routes.
-We generate warp routes for the newly deployed token connecting the parent and destination chains of interests.
- Bridging of token is handled via hyperlane cli. The whole logic of working with the cli is abstracted with go scripts and shipped in the container image.
- Finally the deployement of LP pools happen via JS scripts again and this step is also part of the docker image and shipped in it.

 
## Deployer Address:

The deployer address used to deploy warp routes and several other tokens on each chain are:
- 0xfb01313Ef6FC6e683d1408E98c93B19d9C16F1BB
- 0xd799db5dF493C7c03D70a14e78462F5Dfaa0f063

## Celo Walllet Address 

The address used to deploy various ERC20 tokens: 
- 0xbe66842C517c6DAc6693b0EFB17294cbb8Eb81B4

## Uniswap Contract Address for Celo Alfajores

UniswapV3Factory:
 - 0x229Fd76DA9062C1a10eb4193768E192bdEA99572 [Link](https://alfajores.celoscan.io/address/0x229Fd76DA9062C1a10eb4193768E192bdEA99572)
 
NonfungiblePositionManager:
 - 0x0eC9d3C06Bc0A472A80085244d897bb604548824 [Link](https://alfajores.celoscan.io/address/0x0eC9d3C06Bc0A472A80085244d897bb604548824)

## Token and Pool address on Celo testnet

Erc20 tokens :
- 0x36Da2732a33d2E9A2422E0814f009FA08D07245c
- 0x584d543CD91CFa547ae33a9c0cFF970260ac9696

Pool Address : 
- 0x5080546E4E20bD1C984e096d249Fb866Dbe6A7B6
- 0x93f6d57Eb06EB00789D99af001f5aCA81b0dCd48

All these address can be verified on : https://alfajores.celoscan.io/



