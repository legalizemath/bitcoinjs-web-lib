# bitcoinjs-web-lib

bip32 1.0.4 used bc new ones require wrapping tiny-secp256k1 which gives me errors

```
npm i -g browserify uglify
npm i bitcoinjs-lib bech32 bip21 bip32@1.0.4 bip38 bip39 bip44 bip68 bip69 base58 base58check merkle-lib
```

```
const Bitcoin = require('bitcoinjs-lib')
Bitcoin.bech32 = require('bech32')
Bitcoin.bip21 = require('bip21')
Bitcoin.bip32 = require('bip32')
Bitcoin.bip38 = require('bip38')
Bitcoin.bip39 = require('bip39')
Bitcoin.bip44 = require('bip44')
Bitcoin.bip68 = require('bip68')
Bitcoin.bip69 = require('bip69')
Bitcoin.base58 = require('base58')
Bitcoin.base58check = require('base58check')
Bitcoin.Buffer = Buffer
Bitcoin.merkleLib = require('merkle-lib')

module.exports = Bitcoin
```
Accessible in browser via `Bitcoin` global
