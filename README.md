# bitcoinjs-web-lib

bip32 1.0.4 used bc new ones require wrapping tiny-secp256k1 which gives me errors

```
npm i -g browserify uglify
npm i bitcoinjs-lib bech32 bip21 bip32@1.0.4 bip38 bip39 bip44 bip68 bip69 base58 base58check bitcoinjs-message js-lnurl merkle-lib
```

```
const Bitcoin = require('bitcoinjs-lib')
Bitcoin.bech32 = require('bech32')
Bitcoin.bip21 = require('bip21')
Bitcoin.bip32 = require('bip32') // how to avoid "ecc.isPoint is not a function" w/ v3+ needing tiny-secp256k1??
Bitcoin.bip38 = require('bip38')
Bitcoin.bip39 = require('bip39')
Bitcoin.bip44 = require('bip44')
Bitcoin.bip68 = require('bip68')
Bitcoin.bip69 = require('bip69')
Bitcoin.base58 = require('base58')
Bitcoin.base58check = require('base58check')
Bitcoin.Buffer = Buffer
Bitcoin.message = require('bitcoinjs-message')
Bitcoin.eccrypto = require('eccrypto')
Bitcoin.lnurl = require('js-lnurl')
Bitcoin.merkleLib = require('merkle-lib')

module.exports = Bitcoin
```

used in browser via `<script src="https://cdn.jsdelivr.net/gh/legalizemath/bitcoinjs-web-lib@8b2b863981d17c3807f3535cf0a1a8fd24652915/bitcoinjs-lib-browserified.js"></script>`

replace 8b2b863981d17c3807f3535cf0a1a8fd24652915 with whatever commit hash version needed

Which then becomes available via `Bitcoin` global
