# Zksync Payment Link

This is an MVP project created for the [Gitcoin zksync payment link](https://gitcoin.co/issue/matter-labs/zksync/258/100024169)

The zksync payment link app is a single static html file with the intention to keep it simple so that it can be uploaded to IPFS using the [meeseeks-app](https://github.com/ricmoo/meeseeks-app).

# Design

There are 2 forms in the app: the zksync payment link builder form and the payment form.

## Link Builder Form

This form is presented if the url does not contain a hash tag (#). So, this is a default page to display. The form takes in an Ethereum address and the network environment to generate the payment page link with arguments of address and network encoded in the hash of the url.

Users can click on the generated link to go directly to the payment page or copy the link.

## Payment Form

This form is presented if the url contains a hash tag with network and address information. Clicking the pay button on this page with the amount information filled out will bring up the zksync payment page.

If the url hash tag is missing network or address information, users will be redirected back to the link builder page.

# Demo

This app has been deployed on github pages and IPFS.
To access the app from github pages: click the following link

[https://yuetloo.github.io/zkpayment/](https://yuetloo.github.io/zkpayment/)

To access from IPFS, use the following [https://0xgb3b2jvcrtfjdufyrhvwsfon45ejjowcrqunycrvcjrql63dartmk.meeseeks.app](https://0xgb3b2jvcrtfjdufyrhvwsfon45ejjowcrqunycrvcjrql63dartmk.meeseeks.app)

Another option from IPFS is to go to [meeseeks.app](https://meeseeks.app/) and enter the hash `QmeEnVJ4py3fnJmtUNZt746UsghrBd7PZfkvJTEEDriAjB`.

Here's a youtube demo showing how generate the payment, setup github donation with the link and make a donation using that link.
[![watch zksync payment setup video](https://img.youtube.com/vi/UwkXT4tG6OE/0.jpg)](https://www.youtube.com/watch?v=UwkXT4tG6OE)

# How to deploy to IPFS

2 simple commands to deploy this app to IPFS using meeseeks cli:

```
npm install -g meeseeks-cli
meeseeks-cli publish index.html
```

Result:

```
Publishing: index.html (14021 bytes)
  Hash: QmRa1LkShQmZG7SrssaUsQPCkNVWtuSrFVdAxE8ChW4mCv
  URL:  https://0xgl766ci4gkm4ogwsqn64qg2tiomz6wc6vpsfp5l7zdjtrzi7dbdl.meeseeks.app
```

# TO-DO

1. More testing
   So far, I only tested the app on roptens and rinkeby using the ETH token.

1. Add description to the zksync transaction

1. ENS integration

# License

MIT
