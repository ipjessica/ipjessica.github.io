---
layout: post
title: A High-Level Exploration of Data Availability Options for Layer 2 Rollups
---

Layer 2 (L2) scaling protocols such as rollups employ a method that processes data and computations off-chain to increase throughput and reduce transaction costs on the main (L1) network. Persistent in rollups and other off-chain scaling solutions, the vulnerabilities that stem from inaccessible and unverified data can be characterized as the data availability problem: the assurance that verified transaction or state data stored off-chain can be retrieved when required.

As modular blockchains are increasingly prevalent, such as ones that specialize in preserving other chains’ data, ensuring secure data availability mechanisms is crucial for the successful utility of rollups. Data availability options for L2 rollups today can be categorized as either on-chain or off-chain. On-chain means that rollups store all transaction data on the L1 chain, thus inheriting the security of L1 nodes. Off-chain methods verify data availability without the need for any node to download all of the data, and can be further differentiated into two techniques: Data Availability Committees (DACs) or Data Availability Sampling (DAS). 

DACs are trusted sets of nodes that store copies of data offline and vouch for data availability by publishing attestations on-chain. In the case of a dispute, DACs make the data available for settlement. For instance, EigenLayer’s EigenDA is a decentralized data store that does not require independent consensus to solve, with storage of rollup transactions handled off-chain by trusted EigenDA operators. The weakness around DACs is the reliance on the proper functioning of nodes to ensure data availability, heavily dependent upon a trust assumption. Developments to address this challenge are in progress, with one such proposal leveraging financial incentives to deter malicious behaviour (Tas and Boneh, 2023).

DAS on the other hand, necessitates that each node (including non-staking nodes) download a small amount of the total data to sample. This in comparison to DACs requires the data sampling to be done by the client as opposed to by the network. Celestia is a data availability layer that features DAS by having light nodes randomly sample full nodes; as more rounds of sampling are completed, then it is likely that the whole block’s data is available. However, DAS suffers from the same trust assumption vulnerability that plagues DACs as DAS queries for data must await response from DAC nodes. 

DAS can be used alone or in conjunction with DACs, as each techniques has its own strengths and weaknesses contingent upon the circumstances. While DACs and DAS are methods that ensure the availability of off-chain data, proofs ensure the integrity and accuracy of the data. Validity proofs are used by zero-knowledge rollups to provide evidence of the correctness of off-chain computations, whereas fraud proofs are common in optimistic rollups to detect and prove the fraudulent nature of specific transactions or states.

Ultimately there are many data publishing solutions, but crucially, they do not provide a guarantee of consensus about data availability or publish date. While the proposed data availability policies each have their tradeoffs, a combination of techniques will be required for L2 rollups to not only maintain data availability, but data validity as well.

<h5><ins>References</ins></h5>
Al-Bassam, M., Sonnino, A., Buterin, V. (2019) Fraud and Data Availability Proofs: Maximizing Light Client Security and Scaling Blockchains with Dishonest Majorities. <a href="https://arxiv.org/pdf/1809.09044.pdf">https://arxiv.org/pdf/1809.09044.pdf</a><br>

Awosika, E. (2023, December 20). <i>Data Availability Or: How Rollups Learned To Stop Worrying and Love Ethereum.</i> <a href="https://ethereum2077.substack.com/p/data-availability-in-ethereum-rollups">https://ethereum2077.substack.com/p/data-availability-in-ethereum-rollups</a><br>

Celestia Docs. (2024, March 21). <i>Blobstream: Streaming modular DA to Ethereum.</i> <a href="https://docs.celestia.org/developers/blobstream">https://docs.celestia.org/developers/blobstream</a><br>

EigenLayer Docs. (2024). <i>EigenDA Overview.</i> <a href="https://docs.eigenlayer.xyz/eigenda/overview">https://docs.eigenlayer.xyz/eigenda/overview</a><br>

emmanuel-awosika. (2023, December). <i>A taxonomy of data availability policies in (Ethereum) rollups.</i> [Online forum post]. Etc Research. <a href="https://ethresear.ch/t/a-taxonomy-of-data-availability-policies-in-ethereum-rollups/17949">https://ethresear.ch/t/a-taxonomy-of-data-availability-policies-in-ethereum-rollups/17949</a><br>

Ethereum. (2024, January 14). <i>Data Availability.</i> <a href="https://ethereum.org/en/developers/docs/data-availability/">https://ethereum.org/en/developers/docs/data-availability/</a><br>

Huang, C., Song, R., Gao, S., Guo, Y., Xiao, B. (2024). Data Availability and Decentralization: New Techniques for zk-Rollups in Layer 2 Blockchain Networks. <a href="https://arxiv.org/pdf/2403.10828.pdf">https://arxiv.org/pdf/2403.10828.pdf</a><br>

Nijkerk, M. (2023, July 12). <i>What Is Ethereum’s ‘Data Availability’ Problem and Why Does It Matter?</i> <a href="https://www.coindesk.com/tech/2023/07/12/what-is-ethereums-data-availability-problem-and-why-does-it-matter/">https://www.coindesk.com/tech/2023/07/12/what-is-ethereums-data-availability-problem-and-why-does-it-matter/</a><br>

Tas, E. N., & Boneh, D. (2023). Cryptoeconomic Security for Data Availability Committees. Financial Cryptography and Data Security, 310–326. <a href="https://doi.org/10.1007/978-3-031-47751-5_18">https://doi.org/10.1007/978-3-031-47751-5_18</a><br>

vbuterin. (2024, January 16). <i>An explanation of the sharing + DAS proposal.</i> <a href="https://hackmd.io/@vbuterin/sharding_proposal#Why-not-use-just-committees-and-not-DAS">https://hackmd.io/@vbuterin/sharding_proposal#Why-not-use-just-committees-and-not-DAS</a><br>
