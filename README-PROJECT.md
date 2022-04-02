# node-web3
A fully featured & asset-centric abstraction layer for interacting with web3 wallets in node. Node-web3 is a collection of opinionated and intuitive interfaces for the various components of the web3 stack, including wallets, assets (native & ERC), contracts & pools.

#### Submodules:
- @node-web3/factory
- @node-web3/asset
- @node-web3/native
- @node-web3/erc20
- @node-web3/wallet
- @node-web3/contract

---

#### Usage example (DRAFT)
```
let { Wallet, ERC20 } = require('@node-web3/factory');
let wallet = Wallet('aaa', 'key'); //private
let recipient = Wallet('bbb'); //public
let dai = ERC20('dai');

let tx = wallet.send(
                    recipient, // Wallet 
                    dai, // ERC20 Token
                    dai.toWei(11.5) // => 11500000000000000000
                    )

if (tx.success) {
    // All good
}
```