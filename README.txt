______    _______  _______  ______   __   __  _______
|    _ |  |       ||   _   ||      | |  |_|  ||       |
|   | ||  |    ___||  |_|  ||  _    ||       ||    ___|
|   |_||_ |   |___ |       || | |   ||       ||   |___
|    __  ||    ___||       || |_|   ||       ||    ___|
|   |  | ||   |___ |   _   ||       || ||_|| ||   |___
|___|  |_||_______||__| |__||______| |_|   |_||_______|

================================================================

### What this is 
================================================================
A fun DApp! Essentially, it's a never-ending, public, distributed, blockchain-based game of the card game
What Do You Meme(https://whatdoyoumeme.com/), where participants compete to create
the funniest meme by pairing the best Caption Card with the Photo Card in play.

In the traditional game, a rotating centralized judge is chosen to determine which
Caption Card best completes the Photo (Meme) Card in play. That obviously makes which
card wins very subjective to the judge's sense of humor, rather than that of all the
participants. So in my decentralized version, I wanted all participants to have a
role in deciding which card wins the round. So keeping this in mind, I designed
the Caption Cards in this game to be bonding curve contracts that issue
continuous ERC20 tokens. This provides each caption card with the properties of
limitless supply and instant liquidity- can be bought and sold at any time according
to a price determined by the curve- which make them ideal for this sort of game.
Because the price is based on a bonding curve, it will rise as players buy into it
and fall as they sell it, giving the most popular card the highest price.

In the game, each round looks like this:
- Each round of the game lasts 24 hours
- A Meme (Photo) Card is chosen at random each round (sadly this is centralized
at this point in time, might eventually look into ways to design this so it can
be decentralized)
- Players can either buy into an existing Caption Card that they think best
completes the current Meme Card in play, or create a new one
- They can also sell cards that they don’t think fit with the current Caption Card
- At the end of the round, the Caption Card with the highest price is the winning card

This encourages the curation of good content, and rewards content creators
and those with a good sense of humor who buy into a funny card early on.

### Project Takeaways
================================================================
All in all, I learned so much building this somewhat distributed DApp, which
is currently deployed on the Ropsten Test Network and can be accessed here:
https://what-do-you-crypto-meme.herokuapp.com/. 

While it was definitely a more challenging experience than I expected, I had a lot
of fun building this project, and perhaps got way too into it. Each stage of this
project included a lot of learning by reading medium articles and doing, and I'm looking to building
more DApps in the future and perhaps making this one even more decentralized.


### Instructions of how to run 
================================================================

### Solidity Contracts and Tests ###

The solidity contracts for this project are in the contracts folder.
Tests for these contracts are contained within the test folder. In order to run
these tests:

in the top level directory (WhatDoYouMeme)
run 'npm install'

## upgrade the solidity compiler in truffle by running these commands
cd node_modules/truffle
npm install solc@0.5.2

then cd back into WhatDoYouMeme top level directory and run
'export PATH=$(npm bin):$PATH'


## spin up a private blockchain on your computer with ganache
open a new terminal tab and
run 'export PATH=$(npm bin):$PATH'
run the command ‘ganache-cli’

Wait till you see ‘Listening on 127.0.0.1:8545’

## Return to other tab and run tests by:
running the command 'truffle test' and see that all 10 tests pass

### Running the front end and server ###


### Run the server in development mode
run `npm start` in the top level directory (WhatDoYouMeme)

### Then run the front end app in development mode
open another terminal
cd into the client directory
run 'npm install'
run `npm start`

Open [http://localhost:3000](http://localhost:3000) to view it in the browser.
And interact with the site.

### Note: You must have metamask installed, be logged in, grant the app access
to your accounts, and be on the Ropsten Test Network to use the site.
If you login, change network, etc refresh the site to get rid of the pink banner
and access the actual site.
If you have difficulty accessing the site, it is possible that you have privacy mode
enabled, to unlock:
Settings -> security and privacy -> switch off privacy mode

### See the live version of the app deployed at:
https://what-do-you-crypto-meme.herokuapp.com/
