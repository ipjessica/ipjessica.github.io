---
layout: post
title: Ethereum's Transition from PoW to PoS
---

As part of Ethereum's transition from the Proof-of-Work to the Proof-of-Stake consensus mechanism, it currently has two chains running in parallel: a PoW chain, the chain most users are currently interacting with and where smart contracts are deployed; and a PoS chain that has been in Ethereum's plan since its inception and has been deployed since December 2020. Due to the vast amount of activity and applications and assets that run on the network, it is a delicate and deliberate process in attempting to merge a beacon (PoS) chain (seamlessly) with a live (PoW) chain, one that will continue to transact up until the point where the merge occurs. The PoS chain now has tens of billions of dollars securing it, with blocks that contain metadata about the chain and algorithm itself, but no end user transactions. 

<h5><ins>Terminal Total Difficulty</ins></h5>
The procedure behind the merge is that while the execution layer (PoW) is still running with all of the applications on it, change the rules by which the chain decides how to create a new block. The moment that the execution chain stops listening to the execution layer and looks to the consensus layer (PoS) for achieving the next block is a result of reaching the terminal total difficulty (TTD) value, which is the sum of every single block's hash rate difficulty, tracked since Ethereum's genesis block. This value is the threshold for the merge because rather than using the block number to decide the moment to switch, the difficulty value is much more computationally costly to fake. With just the block number, it may be that a miner could be secretly mining a minority fork for months until that block number is reached (if it happens that the difficulty of that fork has been sufficiently lowered), at which point, the emergence of that block would lead to conflicting forks. 

Therefore, the fork with the first block that hits the threshold value is the final valid PoW block, since the highest difficulty value is the best indicator of the longest chain, and the validator on the PoS chain tasked with creating the next block will begin to include end user transactions and smart contracts, which should be an instantaneous process from the perspective of the Ethereum chain. The merge is considered to be complete once the first block achieved through the PoS consensus mechanism has reached finality.

<figure>
    <p>
        <img src="/assets/images/EthMergeDevnets.png" alt="Ethereum Merge Devnets"/>
        <figcaption>merge-devnet-4: There can be multiple TTDs because uncle blocks are an integral part of Ethereum, helping to secure the network and allow for shorter block times. <a href="https://www.ethereumcatherders.com/" target="_blank" rel="noopener noreferrer">Ethereum Cat Herders</a></figcaption>
    </p>
</figure>

<h5><ins>Difficulty Bomb</ins></h5>
Not all miners may be quite so eager to switch to PoS due to the possibilty of reduced profits as compared to PoW. The impetus behind incentivizing them to migrate is the difficulty bomb, a critical feature of the merge plan. It is an overhead that the network adds to the hash rate difficulty (analogous to adding fake miners on the network) at an exponential rate. Once the bomb "goes off," it is a gradual process at first, with miners requiring more and more time to validate transactions. Within 8-10 weeks, the difficulty becomes even greater than the sum of all of the blocks' difficulties, such that mining on the PoW chain becomes impossible as it cannot coexist alongside the beacon chain following the chain-split. Ethereum node users will have to update both their execution and consensus layer clients to accommodate the latest software, followed by manually overriding the TTD value on their clients.

<figure>
    <p>
        <img src="/assets/images/EthBlocksPerWeek.png" alt="Ethereum Block Production Per Week"/>
        <figcaption>Ethereum Block Production Per Week, from <a href="https://dune.com/yulesa/Blocks-per-Week" target="_blank" rel="noopener noreferrer">Dune Analytics</a></figcaption>
    </p>
</figure>

To accompany the graph is this <a href="https://ethresear.ch/t/blocks-per-week-as-an-indicator-of-the-difficulty-bomb/12120" target="_blank" rel="noopener noreferrer">thread</a> that analyzes how the number of blocks produced per week can be an indicator of whether the bomb will go off soon. Where there are dips in the graph, the bomb has previously gone off, causing a decrease in block production with an inverse correlation to the increasing hash rate difficulty. Before the bomb reaches the threshold value however, each time the Ethereum dev team has delayed that fateful date, with the most recent <a href="https://eips.ethereum.org/EIPS/eip-5133" target="_blank" rel="noopener noreferrer">delay</a> being pushed to mid August, citing continued issues on the client side and with edge cases.

<h5><ins>Shadow Forking</ins></h5>
Historically, whenever there have been upgrades, Ethereum will deploy testnets to test on, then utilize existing testnets such as Ropsten, Rinkeby and Goerli. But nowadays, even the testnets themselves have as much activity as actual layer-1 blockchains. Shadow forking enables the duplication of another network, the state included (devnets, while similar, have their own state). The upgrade is launched on an existing network, but only using a small number of nodes. Ultimately forking off once a certain block number is reached, the shadow fork continues to receive mainnet transactions and other state information.

<h5><ins>End in Sight?</ins></h5>
As mentioned, a successful transition to PoS is particularly precarious, given the Massive weight of any security vulnerability in a blockchain, amongst all of the unknown issues that will befall the dev team, with the incredible amount of value that sits on the blockchain presently. The delays can be attributed to having to ensure that all of the shadow forks and testnets have no issues before moving onto forking of the mainnet, all while providing releases and giving users time to update their nodes. Because this process alone could easily take at least two months, Vitalik has made mention of whether it might be worth it to withstand the long (~20+ seconds) block times, if that means not having to announce another delay, believably for reasons around optics. As far as current progress goes, the Ropsten network will undergo the merge <a href="https://blog.ethereum.org/2022/06/03/ropsten-merge-ttd/" target="_blank" rel="noopener noreferrer">today</a> , marking the final phase of testing before deploying to mainnet.

<br />
Sources:<br />
<a href="https://youtu.be/5mMd-XHAv2Q" target="_blank" rel="noopener noreferrer">Ethereum Core Devs Meeting #139 [2022-5-27]</a><br />
Unchained Podcast - <a href="https://unchainedpodcast.com/why-ethereums-merge-was-delayed-and-why-it-wont-reduce-gas-fees-much/" target="_blank" rel="noopener noreferrer">Why Ethereum's Merge was Delayed and Why It Won't Reduce Gas Fees Much</a><br />
<a href="https://seekingalpha.com/article/4501929-what-shadow-forks-mean-for-ethereum-merge" target="_blank" rel="noopener noreferrer">Shadow Forking</a><br />
