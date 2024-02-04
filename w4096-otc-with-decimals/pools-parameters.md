# Pool's parameters

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

1. Every pool has an available amount of w4096 in it. For the pool displayed above, it is **2.86 w4096**.\
   This is the maximum amount that you can buy from this pool.
2. The price of the pool above is **0.1221 ETH** for 1 w4096 token. Meaning if you want to buy 0.5 w4096 from this pool, you would pay 0.06105 ETH - the half of it.
3. The "Range" parameter displayes the MIN and MAX price for the pool. Pool's price will always follow the original live 4096 price on Uniswap, but only within the pool's boundaries.

{% hint style="info" %}
For example, "**Range: 0.108e - 4096e**" means that the pool price cannot get lower than **0.108 ETH** for 1 token and cannot get higher than **4096 ETH** for 1 token.\
Anything in between and the price will be synced with the price of 4096 on Uniswap.
{% endhint %}

4. The % of ETH amount displayed in parentheses is the additional price or a discount relative to the live 4096 price on Uniswap.

{% hint style="info" %}
For example, _**(+4%)**_ means that pool has a **4%** larger price than live 4096 price and _**(+0.01e)**_ means that the price is bigger by a fixed amount of **0.01 ETH**.

If you see a "**-**" sign instead of a "**+**" sign, it is because there's no additional price but a **discount**. So the price of the pool is actually **less** than the live original price of 4096.

This is useful for whitelisted pools created exclusively for a selected address, of if you just want to sell your tokens quicker.
{% endhint %}

{% hint style="info" %}
**Example 1:** if the pool has a range of 0.1-0.2 ETH, additional price of 0.01 ETH and the current market price of 4096 on Uniswap is 0.15 ETH, then the pool's price will be equal to 0.16 ETH.
{% endhint %}

{% hint style="info" %}
**Example 2:** if the pool has a range of 0.1-0.2 ETH, discount of 0.05 ETH and the current market price of 4096 on Uniswap is 0.12 ETH, then the pool's price will be equal to 0.1 ETH.\
If there was no MIN restriction of 0.1 ETH, then the price would be 0.12-0.05 = 0.07 ETH. The final price cannot be lower than its MIN boundary, so that's why it's gonna be 0.1 ETH.
{% endhint %}
