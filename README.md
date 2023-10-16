# solidity-smart-contract-examples

---------- 10-16-2023 ------------------
Decentralized cupcakes demo project. 
There were 2 errors after deploying the contract:
1) Error: Transaction reverted: function selector was not recognized and there's no fallback nor receive function
2) eth_estimateGas
* in hardhat.config, added property - initialBaseFeePerGas: 0 - (for eth_estimateGas) FIXED.
* in VendingMachine.sol, added functions - receive() and fallback() - (for function selector not recognized, no fallback nor receive) FIXED.
Still unable to get metamask pop-up to sign the transaction from front-end after inputting contract address to receive cupcake,
seems to be Hardhat local node issue only. Should work on Testnet/Mainnet without issues per forums.
Transactions directly in Metamask working fine.


------------ 10-14-2023 ------------------ 
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
