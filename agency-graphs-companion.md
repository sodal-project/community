# Agency Graphs: Utility, Limits, and Open Work
Andy Schwab, Sodal, Inc. (2024-2026)

*Companion note to `agency-graphs-paper.md`.*

This note situates the paper against adjacent work, describes what the framework has been useful for in practice, and identifies where the most interesting open questions sit

---

## What This Is In Conversation With

This paper was not developed through a systematic survey of the relevant literature. It emerged from practical attempts to manage identity, trust, and access across heterogeneous systems in settings where no single authority controlled the whole environment. As a result, some elements restate or rediscover ideas that already exist in adjacent domains.

The contribution claimed in the paper is not the invention of graph-based authorization, decentralized credentials, probabilistic trust, or cryptographic attestations - all of which have been developed in considerable depth previously. Rather, the paper aims to synthesize these domains into a common framework, and then use that framework for two interconnected purposes: (1) to describe the relationships between volitional actors in complex systems and (2) to provide a richer model for reasoning about outcomes in those systems.

The paper is therefore in conversation with several established or emerging areas:

- Relationship-based authorization and graph access systems such as Zanzibar and ReBAC ([AuthZed overview](https://authzed.com/blog/exploring-rebac), [AWS overview](https://aws.amazon.com/blogs/database/graph-powered-authorization-relationship-based-access-control-for-access-management)). The earliest work leading to the paper began by exploring whether Zanzibar could be adapted not to enforce but to discover, describe, and illuminate cascading relationship change effects.
- Decentralized identity, DIDs, and verifiable credentials as ways to raise identity fidelity and portability.
- Zero Trust, trust-score, and risk-adaptive access work ([trust score-based Zero Trust access control](https://www.mdpi.com/2076-3417/15/17/9551), [network-level trust score access control](https://arxiv.org/abs/2402.08299)). A key point of friction with these domains was the need to support, from the very beginning, pluralistic definitions of authority, trust, and risk.
- Trust and reputation networks, including probabilistic trust formalisms such as [subjective logic](https://en.wikipedia.org/wiki/Subjective_logic) and trust-network analysis ([Jøsang trust network analysis](https://www.mn.uio.no/ifi/english/people/aca/josang/publications/jhp2006-acsc.pdf))
- Provenance and cryptographic attestation efforts in software supply chain and identity ecosystems
- Decentralized reputation efforts such as [TrustGraph](https://trustgraph.net/)

Agency graphs attempt to synthesize these concepts around a problem that has remained only partially solved: community management across heterogeneous systems with no single authority, imperfect trust, and cascading delegated control.

## What Is Useful Now

I hope this paper provides a useful way to reason about several real problems.

First, it reframes cross-platform community management as a graph of delegated control rather than as a directory-sync problem. That helps explain why conventional IAM, role assignment, or platform-specific automation often fail to adequately support communities that live across diverse chat, code hosting, cloud systems, documents, wallets, and human relationships.

Second, it makes downstream agency visible. That is useful for access review, lifecycle changes, bad-actor containment, AI agent oversight, and hidden dependency concentration. In current security language, parts of this overlap with blast-radius and attack-path analysis, but the paper extends that logic beyond adversarial escalation into general collaboration and trust formation.

Third, it treats attestation, reputation, and verification as inspectable inputs rather than as opaque scores. That preserves a central role for human judgment while still making the inputs to trust decisions more legible.

Early internal implementations of this framing were able to deliver useful capabilities in customer settings, but they did so with primitive quantitative machinery. The certainty layer was closer to simple presets and heuristics than to a mature or general model. Those efforts are best understood as exploratory artifacts rather than as robust embodiments of the theory, even when they were practical enough to solve real problems in context.

## What Remains Open

### Certainty Math Is Still Open, But Not In The Sense Of Finding One True Formula

The paper needs a quantitative vocabulary for certainty. It does not need a single universal algorithm. Different use cases have different data qualities, stakes, attack models, and social assumptions. A consumer email-trust heuristic, a community onboarding model, an open source supply-chain model, and an AI action-approval model may all require different methods.

The more durable goal is therefore modularity. An agency-graph implementation should be able to combine:

- Evidence inputs
- Evidence provenance and quality
- Local composition within a persona or edge
- Path propagation across controller relationships
- Operator policy for decisions, thresholds, and interventions

This makes certainty a competitive and experimental layer rather than a fixed doctrine. Some implementations may use weighted heuristics, some Bayesian or subjective-logic-style models, some domain-specific rules, and some hybrid approaches. The framework should make those choices explicit and replaceable.

What is missing is a way to describe this modular space quantitatively enough that implementations can be compared, audited, and improved without forcing them into one algorithmic mold.

### Path Semantics And Query Semantics

The paper says agency cascades, but does not yet formalize how access level, authorization minimum, certainty, and path length should compose across multi-hop or cyclic relationships. This is essential for turning the framing into a more rigorous graph model. Real-world development identified practical directions for refinement, but this work was not finalized.

### Operator Plurality And Disagreement

Operator plurality is a design principle, not an accident. But plural graphs raise hard questions: how independent views interoperate, how conflicting assertions are preserved, how minority views avoid being washed out by dominant operators, and how communities decide which graph to rely on in which context. As with the certainty math, the opportunity is to enable modularity and reduce coordination friction - but without turning disagreements into failure-states. Operators are expected to disagree, and that disagreement is signal too.

### Native Threat Modeling

The paper argues that conventional threat modeling inherits assumptions that agency graphs are challenging. For this critique to become constructive, it needs a replacement vocabulary, but that vocabulary has not yet been developed. A native threat model for probabilistic, graph-based agency remains open terrain.

### Interoperability And Naming

Universal Persona Names may be useful, but naming is downstream of deeper questions about provenance, collision handling, schema evolution, and partial interoperability across non-canonical graphs. It was necessary to develop provisional naming to conduct practical experiments, but the structure of UPNs is not central to, and may be a distraction from, the broader framework.

### Applied Case Studies

The concepts will get sharper if future work tests the framework in bounded domains. Promising areas include cross-platform community lifecycle management, AI-agent governance, and open source supply-chain risk. Each would stress different parts of the model, refining key concepts while clarifying implementation considerations.

## Where Work Could Go Next

The next stages of work likely fall into three buckets.

First, editorial work: position the paper against adjacent domains, clarify claims, and make the release boundary explicit.

Second, formal work: define modular certainty interfaces, evidence classes, composition rules, and query or path semantics.

Third, applied work: build small, domain-bounded case studies that use different certainty approaches and compare their strengths, weaknesses, and failure modes.

The important thing is not to force premature closure. The value of this line of work may lie less in converging quickly on a standard and more in opening a space where community management, identity, trust, and delegated control can be reasoned about together without collapsing back into atomic identity or centralized authority.

This note is being released in that spirit: not as a claim of completeness, but as an attempt to preserve a framing that I hope is worth continuing to explore.
