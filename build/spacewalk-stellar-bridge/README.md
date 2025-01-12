# Spacewalk (Stellar bridge)

Spacewalk enables the Pendulum chain to utilize the multitude of fiat stable tokens on the Stellar blockchain and help build the fiat DeFi future. Spacewalk is the first bridge between the Stellar network and the Polkadot/Kusama ecosystems, which opens up a flow of stable tokens from the Stellar network. Based on the [XCLAIM](https://www.xclaim.io/) protocol and interBTC, it is implemented as a set of Substrate pallets and allows Substrate-based blockchains to implement a direct Stellar bridge.

Spacewalk is a trustless and decentralized bridge built to connect Pendulum and Stellar, but it can also be plugged into any Substrate-based blockchain on Polkadot. That's why, in the following, we will refer to so-called Spacewalk-chains instead of a specific Substrate network like Pendulum.&#x20;

You can read more about the bridge concept and how it works in our [blog post](https://pendulum-chain.medium.com/introducing-spacewalk-the-trust-minimized-bridge-between-stellar-and-pendulum-68ddbe7349a0). In the following, we will focus on the key components required in Spacewalk, which are _Vault_ clients.

{% hint style="info" %}
The following guide uses the provided testchain for convenience. The idea is to illustrate how to connect Spacewalk to a standalone chain. The approach to connecting to the Pendulum chain differs slightly and is addressed in[Broken link](broken-reference "mention").
{% endhint %}

### Video guide for Spacewalk

Following is the video guide on how to bridge using Spacewalk from Stellar to Amplitude and back.&#x20;

{% embed url="https://www.loom.com/share/1d9d5ce1a4cf4ddbbe979e959b4a04be?sid=8ea5bb5b-a970-40c3-890f-3a1de3dcc6bc" %}
