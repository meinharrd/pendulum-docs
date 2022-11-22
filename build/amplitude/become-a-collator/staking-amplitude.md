# Staking Amplitude

```bash
Users’s minimum delegator stake is currently 10 AMPE
```

As of Nov 1, 2022, all AMPE token holders can stake their tokens to participate in the security of the network and in turn, get rewarded.

While there will be a dedicated dashboard for staking, in the meantime users can perform the following actions via Polkadot.js in relation to staking.

In order to stake to the selected pallet users need to first navigate to

1. Developer/Extrinsics;
2. Select `parachainStaking` ;
3. Select an action:

<figure><img src="../../../.gitbook/assets/Screenshot_2022-11-16_at_15.10.58.png" alt=""><figcaption></figcaption></figure>

### Delegating - Join delegators action

In order to join as a delegator a user has to:

1. select the parachainStaking extrinsic
2. select the joinDelegator action
3. Lookup a collator address in order to find them

<figure><img src="../../../.gitbook/assets/Screenshot_2022-11-16_at_15.15.47.png" alt=""><figcaption></figcaption></figure>

To find the collators a user can either:

* Be provided a list of collators
* Look up a list of collators:

1. Navigate to the tab chainstate under Developers/Chainstate
2. There query for: parachainStaking and select the topCandidates() function
3. Select an owner-id as a collator to delegate to

<figure><img src="../../../.gitbook/assets/Screenshot_2022-11-16_at_15.22.22.png" alt=""><figcaption></figcaption></figure>

```bash
Do note that due to the current UI implementation staking X 
amount requires the addition of 12 0s 
Staking 10 → 10 0000 0000 0000
```

A user can appropriately delegate by filling the previous form with one or more of these ids

<figure><img src="../../../.gitbook/assets/Screenshot_2022-11-16_at_15.37.23.png" alt=""><figcaption></figcaption></figure>

The transaction can now be submitted to perform the join delegators action

A user can see a list of their delegations under

1. Navigate to the tab chainstate under Developers/Chainstate
2. There query for: parachainStaking and select the delegatorState() action

### Claiming

The respective method for checking a User’s rewards are under the ChainState tab

1. Navigate to the tab chainstate
2. Query parachainStaking and select the rewards() action

<figure><img src="../../../.gitbook/assets/Screenshot_2022-11-16_at_15.51.34.png" alt=""><figcaption></figcaption></figure>

The rewards can be claimed by:

1. Navigating to extrinsics tab
2. Query parachainStaking and select the claimRewards action

### Increasing and decreasing stakes

1. Navigate to the extrinsics tab and select the respective action
2. Insert the delegator-id to which a user has already delegated and the amount to change

<figure><img src="../../../.gitbook/assets/Screenshot_2022-11-16_at_15.45.48.png" alt=""><figcaption></figcaption></figure>

The new stake will be PreviousStake **± amount**

### Leaving delegator

1. Navigate to the extrinsics tab
2. select the leaveDelegators() action
3. A user can verify the successful completion of the action thorugh:
   1.  The upper right success operation providing feedback\


       <figure><img src="../../../.gitbook/assets/Screenshot_2022-11-17_at_12.00.09.png" alt=""><figcaption></figcaption></figure>
   2. By verifying via the topCandidates action that their stake has been removed from the collator

Before:&#x20;

<figure><img src="../../../.gitbook/assets/Screenshot_2022-11-17_at_11.59.37.png" alt=""><figcaption></figcaption></figure>

After:&#x20;

<figure><img src="../../../.gitbook/assets/Screenshot_2022-11-17_at_12.00.41 (1).png" alt=""><figcaption></figcaption></figure>