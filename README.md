---
description: Project overview
---

# What is 4096

{% hint style="info" %}
**Total supply: 4096**\
**Decimals: 0**
{% endhint %}

A minimum amount someone can trade is 1 whole token. Tokens cannot be divided into smaller parts, like 0.99, 5.5, 80.33 - it only can be, for example, 1, 5, 80.

**Tax: 0% buy & 5% sell**, except for <20 tokens sells due to the token having 0 decimals\
4% of the sell tax is going to burn

## Unique burn mechanics

### Guaranteed burn cycles

As a counter to the tax evasion, there is a guaranteed burn tax every 2/4/8/16 sells depending on the current amount of 4096 tokens in LP pair.

{% hint style="info" %}
There are 3 easy ways of checking the current amount of tokens in LP and the sells counter:

1. On [4096.cash](https://4096.cash) graphics explorer and [app.4096.cash](https://app.4096.cash) on the "Teleport" tab
2. In our [Telegrap group](https://t.me/ERC4096) by typing the `/4096` command
3. On [Etherscan](https://etherscan.io/token/0x4096Fc7119040175589387656F7C6073265f4096?a=0x7c3f018376c7b97cb811cd17aa094052dbee6dbc)
{% endhint %}

For example, if current LP amount is between 256 and 512 (excluding 256 and including 512), every 16 sells there is 1 token that will be taken as a burn tax no matter the amount being sold!

| Tokens in LP | Max burn counter            |
| ------------ | --------------------------- |
| 0-256        | Guaranteed burns are paused |
| 256-512      | 16                          |
| 512-1024     | 8                           |
| 1024-2048    | 4                           |
| 2048-4096    | 2                           |

### LP nukes

{% hint style="info" %}
LP nuke is the process of taking out a token directly from the LP pair and burning it.
{% endhint %}

If there are more than 256 tokens in LP pair, one token is nuked from LP if one of these conditions met:

* 8 hours passed since the previous LP nuke
* There were 1024 tokens in sell volume

Once LP nuke is done, timer and volume counters are reset for the next nuke.
