# 1. OP STACK

## What is Data Availability?

Guarantee that some data will be "available" (i.e. retrievable) during a reasonably long time window. In Optimism's case, the data in question are sequencer batches that validators needs in order to verify the sequencer's work and validate the L2 chain. The finalization period should be taken as the lower bound on the availability window, since that is when data availability is the most crucial, as it is needed to perform a fault proof. "Availability" does not mean guaranteed long-term storage of the data.

## What is Data Availability Provider?

Service that can be used to make data available. Ideally, a good data availability provider provides strong verifiable guarantees of data availability, such as Ethereum call data and EIP4844.

# 2. EigenDA and Celestia

## What is EigenDA?

EigenDA is a data availability which stores rollup transactions until their computed state is finalized. EigenDA's design is inspired by Danksharding(also known as EIP-4844).

EigenDA is a data availability store built on top of [EigenLayer](https://docs.eigenlayer.xyz/eigenlayer/overview/).

## What is Celestia?

Celestia is a modular data availability (DA) network that securely scales with the number of users, making it easy for anyone to launch their own blockchain.


## EigenDA vs Celestia for Solana Layer 2

Solana is known for its high throughput and low latency, making it one of the most scalable Layer 1 blockchains.

When considering integration with Solana, the choice between EigenDA and Celestia might depend on several factors:

- Interoperability: `Celestia`'s blockchain-agnostic and modular approach makes it more versatile for integrating with different blockchain ecosystems, including Solana. Its independence from Ethereum's existing infrastructure means it can be tailored more specifically to Solana's unique requirements.

- Scalability and Flexibility: `Celestia`'s design is inherently focused on scalability and flexibility, aligning well with Solana's high-performance goals.

- Security Model: While `EigenDA` offers unique restaking protocols, Solana's existing robust security model might benefit more from `Celestia`'s specialized data availability focus.

> Celestia announced that their stable version will arrive at the end of this year. We will use `Celestia` for Solana Layer 2 - SuperSol in the future.
