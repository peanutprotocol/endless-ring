# Endless

## Inspiration
This inspiration was the idea of future-proof storage and the tamper-free nature of the blockchain. Although these are very technical terms, the ideas of eternity and immutability have been with us since the dawn of civilisation.

These are also key concepts of love, whether it's affectionate, familiar, brotherly, or romantic love. To express it to family, a friend, or a romantic partner in an eternal and immutable way seems very valuable.

There where three nudges for us. 
1) Hugo having gifted his (non-imaginary) gf a QR code with an IPFS-stored message. 2) A common fraud and extortion technique of changing the underlying URL of an NFT or QR code. Many QR code generator sites wait for you to start using the QR code and then ask for very high sums to keep hosting the URL (e.g. once you've already printed your posters or gear), threating you to show ads otherwise. Dirty. 3) IPFS being absolutely interplanetarily and eternally awesome.

## What it does
This web app connects to your wallet, lets you record your voice, and mint that voice as an NFT rendition of your voice wave on IPFS.

The physical ring is an NFC-enabled ring, which will point to the IPFS. You don't need to charge it. You don't need any special app. Simply get your phone close to the ring and it will play your message.

Oh, the web app also shows you some cool 3d floating rings and fog. I know it's hard to miss, but just wanted to mention that again （￣︶￣）↗　

How we built it
Website
For the frontend, we used flask, tailwind, vanilla js, threejs, vantajs, On the backend, we used:

web3.js, eth-brownie to interact with blockchain
numpy, matploblib and pydub to manipulate the voice data
flask, gunicorn, werkzeug to run server-side stuff
Physical ring
We contacted 8 different suppliers and chose the best looking desings, which are being prototyped right now. Unfortunately, due to the difficulty of soldering around copper wire, there have been delays, but the first prototypes work. We made them work by embedding them in an temperature-absorant plastic inlay, which then gets coated with ceramic. The ring is compatible with all modern smartphones. It can be easily programmed. It has about 100k cycles. It is based on ISO 14443A, 13.56MHz NDEF.

Challenges we ran into
Largest challenge: Hardware getting the physical ring to work with soldering.
Any kind of jewellery making process in proximity to copper wire will break the wire.
Very hard to get the shape right, so for prototype we skipped that part.
Smart contract & IPFS: integrating IPFS storage with recording a voice message on the site and also minting an NFT, all in real time.
Time management!
What we learned
Hugo has learnt how to easily integrate IPFS
Hugo has learnt how to integrate crypto transactions on frontend with metamask and web3.js
Konrad has learnt ThreeJS and a lot of frontend stuff.
Konrad has learnt a lot about NFC technology and jewellery manufacturing
What's next for Endless.place
Finalizing ring design & launching on mainnet! Also, expanding our tech-jewelry lineup to include pendants, bracelets and other stuff.


## Instructions
(Assuming linux terminal. If on windows consider using [WSL](https://docs.microsoft.com/en-us/windows/wsl/install))

1. create local python installation, activate it, and install libraries

```
        python -m venv venv
        source venv/bin/activate
        pip install -r requirements.txt
```

2. go to app/src/ and install npm packages

```
        cd app/src
        npm install
```

<br>

That's it! Now you can run the server, or push to github (autodeploys to render).

<br>

### Useful commands:

```
cd src
npm run build-css
```
⬆️ This will run a script that re-builds tailwind everytime you make a change to the html or css.

```
cd src
npm run local
```
⬆️ This builds the css once and will run the server locally.

```
python app.py
```
⬆️ Same thing as before, just without building the css first.

```
cd src
npm run yeet-it
```
⬆️ This says fuck it, builds the css, adds all files to a git commit, and pushes to github.

