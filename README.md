# Welcome to LazyEyes 👁

![](https://github.com/lazyeyesdao/lazyeyes_nft_minting_dapp/blob/main/Logo.png)

Documentation: https://lazy-eyes.gitbook.io/overview/university/minting-contracts-and-storage-nfts

To find out more please visit:

[📺 TikTok](https://www.tiktok.com/@lazyeyes.site)

[👁 Discord](https://discord.gg/kkDdqRzSgu)

[💬 Telegram](https://t.me/lazyeyesdao_group)

[🐦 Twitter](https://twitter.com/lazyeyesdao)

[ℹ️ Website](https://lazyeyes.site/)

# LazyEyes NFT minting dapp 🔥

This repo provides a nice and easy way for linking an existing NFT smart contract to this minting dapp. There are two ways of using this repo, you can go the simple route or the more complex one.

The simple route is so simple, all you need to do is download the build folder on the release page and change the configuration to fit your needs. (Follow the video for a walk through).

The more complex route allows you to add additional functionality if you are comfortable with coding in react.js. (Follow the below instructions for a walk through).

## Installation 🛠️

If you are cloning the project then run this first, otherwise you can download the source code on the release page and skip this step.

```sh
git clone https://github.com/lazyeyesdao/lazyeyes_nft_minting_dapp.git
```

Make sure you have node.js installed so you can use npm, then run:

```sh
npm install
```

## Usage ℹ️

In order to make use of this dapp, all you need to do is change the configurations to point to your smart contract as well as update the images and theme file.

For the most part all the changes will be in the `public` folder.

To link up your existing smart contract, go to the `public/config/config.json` file and update the following fields to fit your smart contract, network and marketplace details. The cost field should be in wei.

Note: this dapp is designed to work with the intended NFT smart contract, that only takes one parameter in the mint function "mintAmount". But you can change that in the App.js file if you need to use a smart contract that takes 2 params.

```json
{
  "CONTRACT_ADDRESS": "0x3323Ce64c19e2739Ea10f69972D94f1BE0c59258",
  "SCAN_LINK": "https://polygonscan.com/address/0x3323ce64c19e2739ea10f69972d94f1be0c59258",
  "NETWORK": {
    "NAME": "Polygon",
    "SYMBOL": "MATIC",
    "ID": 137
  },
  "NFT_NAME": "Lazy Eyes NFT",
  "SYMBOL": "LES",
  "MAX_SUPPLY": 2222,
  "WEI_COST": 20000000000000000,
  "DISPLAY_COST": 0.2,
  "GAS_LIMIT": 285000,
  "MARKETPLACE": "OpeanSea",
  "MARKETPLACE_LINK": "https://opensea.io/collection/lazyeyes",
  "SHOW_BACKGROUND": true
}
```

Make sure you copy the contract ABI from remix and paste it in the `public/config/abi.json` file.
(follow the TikTok video if you struggle with this part).

Now you will need to create and change 2 images and a gif in the `public/config/images` folder, `bg.png`, `example.gif` and `logo.png`.

Next change the theme colors to your liking in the `public/config/theme.css` file.

```css
:root {
  --primary: #5865F2;
  --primary-text: #b9bbbe;
  --secondary: #5865F2;
  --secondary-text: #ffffff;
  --accent: #36393F;
  --accent-text: #ffffff;
}
```

Now you will need to create and change the `public/favicon.ico`, `public/logo192.png`, and
`public/logo512.png` to your brand images.

Remember to update the title and description the `public/index.html` file

```html
<title>Nerdy Coder Clones</title>
<meta name="description" content="Mint your LES NFT" />
```

Also remember to update the short_name and name fields in the `public/manifest.json` file

```json
{
  "short_name": "LES",
  "name": "Lazy Eyes NFT"
}
```

After all the changes you can run.

```sh
npm run start
```

Or create the build if you are ready to deploy.

```sh
npm run build
```

Now you can host the contents of the build folder on a server.

That's it! you're done.

Base code is from: https://github.com/HashLips