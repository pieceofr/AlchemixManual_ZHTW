# 鎖倉池 (Staking Pools)

*[Offical English Manual-Staking Pools](https://alchemix-finance.gitbook.io/alchemix-finance/token-distribution/staking-pools)

Alchemix 的合成代幣需要深度的流動性來達到最大的效能. StakingPools.sol 智能合約驅動著鎖倉池. 它主要的目的是分發 ALCX 代幣給社群以及在Alchemix 生態裡提供流動性對代幣的人. 

在上架時, 會有4個池, 一個是 alUSD, 一個是 ALCX, 一個是 alUSD/DAI SLP (Sushi Liquidity Pair) 代幣 (註:Sushi 的流動性對), 還有就是 ALCX/ETH 的 SLP 代幣.


以下是建立了各個池的比重還有基本原理:

+ 18% alUSD3CRV-f LP 代幣. 盡可能的建立一個釘著 $1 以及提供深度流動性給 alUSD 是最重要的. 藉由此將給作為先進的收益種植( yeild farming) alUSD 建立一個實際的作用. 讓其可以在低打滑(low slippage)下, 簡單的被轉化成 DAI, USDC, 或是 USDT

+ 60% ALCX/ETH SLP 代幣. 這個幣對的存會給ALCX治理代幣提供流動性市場

+ 2% alUSD 代幣.  這是一個為了激勵使用者持有alUSD直到 alUSD/DAI 幣對成為一個有效的流動而設的最初始的池. 這也提供了一個低風險的管道來獲取 ALCX治理代幣.


+ 20% ALCX 代幣. 這個池是為了獎勵覺得參與ALCX/ETH池太過風險的 ALCX持有者而設. 社群將會決定了這個池的壽命. 

當有越來越多的Alchemix 合成代幣在市場上, 那麼在這些池子還有比重都會被調整. 最重的是激勵合成代幣對與它們的基礎資產.

###### tags: `Defi` `Alchemix` `User Manual` `Tranditional Chinese` `zh_tw`