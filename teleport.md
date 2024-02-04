# Teleport

As it was mentioned in the [beginning](./), there is a guaranteed burn cycle mechanism that occurs every 2/4/8/16 sells depending on the LP pair balance. This burn cycle ensures that every X sells exactly 1 token will be taken as a burn tax.

Teleport is a mechanism to accelerate burns, instantly increasing the burn cycle counter to its maximum.

{% hint style="info" %}
**Example:** sells counter is at 16/16, someone sells and burns a token. So the counter goes back to 1/16.

Now anyone can use the teleport now and instantly set the counter to 16/16, so the very next sell will also burn 1 token.

Otherwise, if there's no teleport used, the next sell will only move the counter to 2/16, but the teleport still will be available no matter the current sell counter (except if its at 16/16 or 8/8).
{% endhint %}

The Teleport will cost its user a gas fee + LP fee. The gas fee for boosting it from 1/16 to 16/16 is around x3 of the normal sell fee on Uniswap. This is achieved by an optimized Teleport contract, so instead of paying 16x sell fees + 1x buy fee, you only pay around 3x sell fee).

The extra LP fee is there due to how Uniswap V2 LP works - it takes 0.3% tax every time that is boosting the LP. So if you sell X tokens, you would pay a bit more to then buy X tokens back and all the extra amount will go directly to the LP boosting its ratio.

Use the teleport at [app.4096.cash](https://app.4096.cash) by going to the "Teleport" tab. Note that the "Max ETH to spend" amount is referring to the LP fee, not to the gas fee.
