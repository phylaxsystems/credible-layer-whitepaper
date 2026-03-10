# The Phylax Credible Layer

We introduce the Phylax Credible Layer, a novel blockchain security
mechanism designed to prevent and mitigate hacks in decentralized appli-
cations by integrating at the network’s base layer. The protocol comprises
two core mechanisms built upon a single primitive: Assertions. These
are out-of-band computations over the base layer’s state, associated with
specific smart contracts, enabled at any time, and computed off-chain,
allowing for a broader range of constraints than possible on-chain. The
mechanisms enable dApps and the base layer to coordinate on valid and
invalid states:

1. The State Oracle (SO): A mechanism where assertions are defined
and associated with specific smart contracts (Assertion Adopters).
Assertion Consumers (Users) can submit proofs about transactions
that invalidate an Assertion, either as Proof of Possibility (potential
future transaction) or Proof of Realization (on-chain executed trans-
action). Proofs are submitted only when an assertion is invalidated.
2. The AssertionEnforcement Mechanism: Actors(AssertionEnforcers)
bond and commit to enforcing that transactions they submit do
not invalidate any Assertion. These can be any entity with trans-
action inclusion veto power, such as block-builders, sequencers, or
searchers. They receive fees for this service and are slashed if a
Proof of Realization is submitted for any state resulting from their
transactions.

This work explores the mechanism’s design space, security model, and
use-cases. It discusses the implementation of the first iteration, Ajax,
designed to integrate with OP-Stack-based rollups. It also examines po-
tential fee structures and token incentive designs to align various Credible
Layer actors. Finally, it briefly explores how integrating the Credible
Layer with a base layer might affect the network’s Fork-Choice Rule or
State Transition Function, enabling "Contract-based Soft-Forking".
This is by no means a complete work or peer-reviewed paper, but
rather a first exploration into the design space of the Credible Layer and
it’s primitives. There are many open questions that we have not ad-
dressed, such as the formalization of the security model and the crypto-
economic design. We hope that this work will serve as a foundation for
future research into the Credible Layer, as we progressively move towards
a production-ready implementation.
