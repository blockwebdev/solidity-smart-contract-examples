# solidity-smart-contract-examples

10-14-2023 
Decentralized Cupcakes project, issues on local contract interactions, unrecognized selector,5 

*from 0xfoobar, Balaji's bet <br>
*bitsignal.sol* -- An immutable smart contract that enables 1M USDC vs 1 BTC bet.

1. Define two addresses to participate in the bet.
2. Deploy the BitSignal smart contract with those two addresses as constructor arguments. This ensures asset isolation between bets.
3. The counterparties can call depositUSDC() and depositWBTC() in either order. The second deposit will finalize the bet and start the 90-day timer.
4. When the timer expires, either party can call settle(), which queries the Chainlink BTCUSD oracle and sends both assets to the winner.

*nftexample.sol* -- For example purposes only! While these contracts are deployable, these are strictly for educational/personal testing purposes only. 
Some included comments have been added and is highly advised to go through the contract for final additions before deployment. Should
be used strictly for testnet!
