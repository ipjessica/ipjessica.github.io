---
layout: post
title: Aptos in Brief
---

<h5><ins>Vision & Origins</ins></h5>
The Aptos blockchain positions itself as ubiquitous as cloud infrastructure, emphasizing security, affordability, and flexibility. To drive web3 adoption, its modular architecture is central to its scalability and high performance.

Aptos was originally called Diem (formerly Libra), a blockchain payment system introduced by Meta. Deployed to over a dozen node operators in early 2020, Meta halted the project two years later, but former employees continued development. Diem then underwent protocol changes alongside its rebranding to Aptos, prior to its mainnet launch in October 2022. It uses a Byzantine fault-tolerant proof-of-stake consensus mechanism, named AptosBFT, a variant of the HotStuff protocol.

<h5><ins>Move Language</ins></h5>
The concept of modularity extends to Move, the programming language originally developed for Diem. Influenced by Rust, Move treats digital assets as customizable resource types with distinct ownership, ensuring proper management. Using move semantics—transferring ownership between variables instead of copying—helps prevent programming errors that could lead to security vulnerabilities. The Move Prover further verifies that smart contracts behave as intended. These contracts can be modular and self-contained, enabling complex applications and enhancing interoperability across different blockchains that adopt Move, such as Sui. 

<h5><ins>Granular State Management</ins></h5>
In most blockchains, the state of the network is updated at the block level, such that when a block of transactions is processed, the entire state of the blockchain is updated. In contrast, Aptos stores the resulting state of each transaction individually, granting more granular access to the data. Users can track the exact version of the blockchain after any particular transaction, rather than just the state after an entire block of transactions has been processed. This would facilitate legal compliance in such circumstances as auditing, as a step towards large-scale adoption.

<h5><ins>Parallel Execution for Scalability</ins></h5>
Fundamental to Aptos’ scalability is its transaction processing approach. Using Block-STM (Software Transactional Memory), transactions can be executed in parallel without advance knowledge of which parts of the blockchain state will be accessed. This method offers greater flexibility compared to traditional parallel execution engines, which demand this data location information beforehand, thereby enhancing processing efficiency.

<h5><ins>Staking</ins></h5>
Staking on Aptos strengthens network security and stability and permits participants to propose or vote on governance protocols, without running a validator node. Voting power is proportional to the amount of APT staked during the current epoch, which currently lasts two hours. The minimum staking amount is 10 APT, plus a small refundable fee. Rewards are distributed to validators and their stakers every epoch, with the highest reward rate at 7%. At a price of $5.95 USD per APT, staking 100 APT for a year would yield $41.65, with auto-compounding provided by Aptos.

Partaking in any crypto ecosystem carries inherent risks due to market volatility. The unbonding period on Aptos is 30 days, meaning tokens can be unstaked anytime but cannot be withdrawn until after this period. To mitigate this, there are liquid staking options available for Aptos, where users receive a derivative token that represents their staked APT, which can be used to earn additional yield.

The minimum to validate is 1M APT, with a maximum of 50M APT. This generally means that validators are staking pools that combine staked APT. It is crucial to research pools when choosing a validator, as the user’s staked APT gets delegated to that pool. Currently, slashing is not implemented. Aptos’ list of pools ranks them by the highest amount of staked APT, indicating trust among delegators, but larger pools may offer lower rewards due to the higher number of participants. Validators charge a commission fee on staking rewards, which varies; a 7% rate is considered reasonable. In the ethos of decentralization, it is advisable to select a staking pool with a lower network share to reduce centralization risks, however, pools with low shares may face profitability concerns over time.

To stake, a wallet must be connected to Aptos’ staking portal. Petra is the official wallet, though other options are available. Once the wallet has sufficient funds, the user can delegate an amount of APT to the chosen pool, where the stake will become active within two hours and begin generating rewards. Users can track their stake balance, history, rewards, and delegations on the portal. Should the user choose to undelegate, they must leave 10 APT in the stake to avoid all of their tokens being withdrawn. Undelegated tokens continue to earn rewards until the pool’s era ends, after which APT can be withdrawn to the wallet. It is recommended to monitor pool performance to ensure maximum rewards, with updates available via Telegram bot.

<h5><ins>Looking Forward</ins></h5>
Aptos’ modular architecture is key to implementing upgrades and optimizations continuously. To scale, it focuses on improving not only individual validator performance, but also sharding at the execution, validator, and blockchain state layers, allowing for more onboarding of validator nodes without network disruptions.

Mainstream adoption is crucial for the future of blockchain, requiring collaboration with non-web3 companies to bring use cases to the public. Aptos’ long-term partnership with Microsoft bridges web3 and AI in areas such as AI-powered assistants, financial services, and Move development. In the entertainment sector, Aptos is aligned with NBCUniversal to introduce blockchain technology through fan experiences in films and games. Additionally, Aptos and Alibaba Cloud are building a Move developer community to teach smart contract programming by hosting educational events to enhance Japan’s web3 network.

<h5><ins>References</ins></h5>
Amsden, Z., Arora, R., Bano, S., Baudet, M., Blackshear, S., Bothra, A., Cabrera, G., et al.(2020). "The Libra Blockchain." <a href="https://diem-developers-components.netlify.app/papers/the-diem-blockchain/2020-05-26.pdf">https://diem-developers-components.netlify.app/papers/the-diem-blockchain/2020-05-26.pdf</a><br>

Aptos. (2024, June 28). <i>Aptos Foundation and Alibaba Cloud Boost Web3 in Japan.</i> <a href="https://aptosfoundation.org/currents/aptos-foundation-and-alibaba-cloud-unite-to-boost-web3-in-japan">https://aptosfoundation.org/currents/aptos-foundation-and-alibaba-cloud-unite-to-boost-web3-in-japan</a><br>

Aptos. (2023, August 09). <i>Aptos x Microsoft Expanding Web3 Global Access.</i> <a href="https://aptosfoundation.org/currents/aptos-microsoft-expanding-web3-global-access">https://aptosfoundation.org/currents/aptos-microsoft-expanding-web3-global-access</a><br>

Aptos. (2022). "The Aptos Blockchain: Safe, Scalable, and Upgradeable Web3 Infrastructure." <a href="https://aptosfoundation.org/whitepaper/aptos-whitepaper_en.pdf">https://aptosfoundation.org/whitepaper/aptos-whitepaper_en.pdf</a><br>

Aptos Dev. (2024, August 15). <i>Governance.</i> <a href="https://aptos.dev/en/network/blockchain/governance">https://aptos.dev/en/network/blockchain/governance</a><br>

Aptos Dev. (2024, August 15). <i>Move Prover.</i> <a href="https://aptos.dev/en/build/smart-contracts/prover">https://aptos.dev/en/build/smart-contracts/prover</a><br>

Aptos Dev. (2024, August 15). <i>Staking.</i> <a href="https://aptos.dev/en/network/blockchain/staking">https://aptos.dev/en/network/blockchain/staking</a><br>

Aptos Dev. (2024, August 15). <i>Delegation Pool Operations.</i> <a href="https://aptos.dev/en/network/nodes/validator-node/connect-nodes/delegation-pool-operations">https://aptos.dev/en/network/nodes/validator-node/connect-nodes/delegation-pool-operations</a><br>

AptoStake. <i>Frequently Asked Questions.<> <a href="https://aptostake.guru/faq">https://aptostake.guru/faq</a> Accessed 2024, August 16.<br>

Consensys. (2022, September 30). <i>Aptos: A highly scalable and decidedly modular Layer 1 blockchain.</i> <a href="https://consensys.io/blog/aptos-a-highly-scalable-and-decidedly-modular-layer-1-blockchain">https://consensys.io/blog/aptos-a-highly-scalable-and-decidedly-modular-layer-1-blockchain</a><br>

Decrypt. (2024, June 20). <i>NBCUniversal Will Continue Building on Aptos via Long-Term Agreement.</i> <a href="https://decrypt.co/236289/nbcuniversal-aptos-long-term-agreement">https://decrypt.co/236289/nbcuniversal-aptos-long-term-agreement</a><br>

IQ.wiki. (2024). <i>Aptos.</i> <a href="https://iq.wiki/wiki/aptos/">https://iq.wiki/wiki/aptos/</a><br>

Nodes.Guru (2023, April 20). <i>AptoStake by Nodes.Guru. How to stake Aptos tokens.</i> <a href="https://www.youtube.com/watch?v=26Pn2-AJBvc">https://www.youtube.com/watch?v=26Pn2-AJBvc</a><br>

Pierro, G. A., Tonelli, R. (2023). "A Study on Diem Distributed Ledger Technology." <a href="https://ceur-ws.org/Vol-3166/paper03.pdf">https://ceur-ws.org/Vol-3166/paper03.pdf</a><br>

Staking Rewards. (2024). <i>Stake APT.</i> <a href="https://www.stakingrewards.com/asset/aptos">https://www.stakingrewards.com/asset/aptos</a><br>

The Move Book. <i>Introduction.</i> <a href="https://move-language.github.io/move/">https://move-language.github.io/move/</a> Accessed 2024, August 16.<br>

Yin, M., Malkhi, D., Reiter, M. K., Gueta, G. G., Abraham, I. (2019). "HotStuff: BFT Consensus in the Lens of Blockchain." <a href="https://arxiv.org/abs/1803.05069">https://arxiv.org/abs/1803.05069</a><br>
