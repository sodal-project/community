# Agency Graphs

- [Mindset and Summary](#mindset-and-summary)
  - [Agency Graphs](#agency-graphs)
- [Concepts](#concepts)
  - [Composite Identity](#composite-identity)
  - [Implicit Roles](#implicit-roles)
  - [Dynamic Agency](#dynamic-agency)
  - [Behavioral Certainty](#behavioral-certainty)
- [Components](#components)
  - [Personas](#personas)
  - [Relationships](#relationships)
  - [Assertions](#assertions)
  - [Universal Persona Name](#universal-persona-name)
- [Example Use Cases](#example-use-cases)
  - [Collaborative Access Management](#collaborative-access-management)
  - [Community Member Lifecycle](#community-member-lifecycle)
  - [Reputation Management](#reputation-management)
  - [Artificial Intelligence Integration](#artificial-intelligence-integration)
  - [Open Verifiability Framework](#open-verifiability-framework)
  - [Improved Zero Trust](#improved-zero-trust)
  - [Open Source Supply Chain Verification](#open-source-supply-chain-verification)
  - [Self-sovereignty](#self-sovereignty)
  - [Collaboration Risk Reduction](#collaboration-risk-reduction)
  - [Systemic Resilience Public Goods](#systemic-resilience-public-goods)

---

## Mindset and Summary

Communities are built on trust. The challenge in building trust is that we cannot be certain what other humans will do. This difficulty exists regardless of the technologies we employ; no technology can completely eliminate the risks associated with human trust building.

The solution objective is to enable fast, effective decision making by reducing information barriers. This allows participants to *focus on trust decisions only humans can make*. The solution achieves this by programmatically generating clarity about the following:

| Layer | DIKW | Question it answers |
|---|---|---|
| **Identifiers** | Data | How we know, or refer to, the people & systems we interact with |
| **Assertions** | Data | How do we correlate identifiers and map attributes in our environment? |
| **Agency** | Information | What can people do with the resources in our environment? |
| **Behavior** | Information | What are people known to do with the capabilities they have? |
| **Certainty** | Knowledge | What degree of confidence do we have in identifiers, assertions, agency, and behavior? |
| **Insights** | Knowledge | Where can we focus to most quickly increase confidence and efficiency in our environment? |
| **Action** | Wisdom | How can we use the previous insights to increase speed and security in our community? |

1. **Identifiers**: how we refer to the agents we interact with
2. **Assertions**: what we know about the agents we interact with
3. **Agency**: what those agents can do with the resources in our environment
4. **Behavior**: what those agents are known to do with the capabilities they have
5. **Certainty**: our degree of confidence in assertions, agency, and behavior
6. **Insights**: where we can focus to quickly increase confidence in our environment
7. **Actions**: how we can use insights to increase speed and security in our community

### Agency Graphs

> **Agency Graphs** are probabilistic graphs of agency in digital systems

The core of our solution is a graph of linked identifiers in digital systems called an agency graph. Agency graphs enable shared resource management by clarifying and managing how influence flows through interconnected digital systems.

Agency graphs use *composite identities* called *personas* to model how participants influence the use of resources within digital systems. We refer to this influence as *agency*. Agency graphs model agency by describing the *relationships* between personas, illuminating when one persona can act on behalf of another persona. The result is a queryable graph of agency informed by every connected digital system.

Participants generate this graph to understand what resources they control, what resources others control, who they are interacting with, and who controls resources they depend on. Participants then use this knowledge to better allocate resources and improve access controls. Agency graphs build on information already available to participants, enabling participants to independently generate and use a graph to improve collaboration.

**A single persona:**

```mermaid
flowchart LR
    subgraph IDRS[Identifier]
        RS[Resources]
    end
    IB[Influenced By] --> IDRS
    IDRS --> IN[Influences]

```

**A persona graph — personas linked by influence:**

```mermaid
graph TD
    P1[Persona] --> P7[Persona]
    P2[Persona] --> P7
    P3[Persona] --> P7
    P4[Persona] --> P8[Persona]
    P5[Persona] --> P8
    P6[Persona] --> P8
    P7 -->|influences| P9[Persona]
    P8 -->|influences| P9
```

---

## Concepts

Agency graph design incorporates four key concepts: composite identity, implicit roles, dynamic agency, and behavioral certainty.

### Composite Identity

> **Composite Identities** are identities that unite identifiers, capabilities, actions, and relationships

Agency graphs assume identity to be a *composite* quality rather than an *atomic* quality. Agency graphs reveal identity through identifiers, capabilities, actions, and relationships. The result is a picture of agency as it cascades through systems.

Participants already use relationship data to improve their understanding of identity in other domains. Examples include running a background check, reviewing a *shared connections* list on a social network app, or analyzing a blockchain wallet's history of activity. An agency graph makes these relationships and related insights integral to the associated identity.

This composite aspect of identity exists in all volitional systems. By explicitly modeling the composite quality of identity, agency graphs expose how agency is already propagating through a participant's environment.

### Implicit Roles

> **Implicit Roles** are roles that emerge organically in a community

An agency graph combines elements of both a social network graph and systems identity management, acquiring properties of both. Like social network graphs, agency graphs model relationships between participants. Like systems identity managers, agency graphs also map access and resource rights information from integrated platforms. This produces a clearer picture of how people and resources are interrelated.

Participants use this picture to identify relationship structures, and then use those structures to understand *implicit* roles. Implicit roles are roles that emerge organically in a community. Once participants identify these roles, they can clarify and improve their composition. This is particularly useful when making trust decisions in the absence of a centralized decision-making authority or prescribed roles hierarchy.

This approach enables greater flexibility than traditional Identity and Access Management (IAM). In order to preserve the utility of an atomic identity, a traditional IAM tool must control every connected system so that it can bring those systems into conformity with the identity's role requirements. This kind of exhaustive, centralized control is incompatible with the goals and structure of many communities. Instead, by incorporating implicit roles, agency graphs enable simplified management while leaving community members free to independently deploy and manage disparate systems and tools.

### Dynamic Agency

> **Dynamic Agency** describes how new data changes our understanding of influence

When a persona's relationships change, so does the persona's ability to access and influence resources in the environment. This quality cascades through downstream persona relationships, with access and permissions configurations informing the degree of impact from a single controller change on an entire set of personas. It is possible for a single modification in an upstream persona's configuration to alter the expected behavior and role suitability of all downstream personas.

Dynamic agency exists whether or not an identity system can model it. Agency graphs illuminate agency dependencies, enabling participants to better align resource access to the participant's risk tolerances. It makes clear, for instance, that participant environments can experience sudden, impactful swings in expected behavior if upstream personas have both low authorization minimums and high access levels.

### Behavioral Certainty

> **Behavioral Certainty** is a measure of our confidence in an agent's expected behavior

The expected behavior of a persona is influenced by many factors. Most of these factors are best described probabilistically: the odds that the user at the keyboard is acting as the expected agent assigned to the active account is never 1:1, but some lesser ratio that is impacted by circumstances ranging from emotional duress to credential compromise. Sometimes, our cats send emails. Rather than describing agent expected behavior in a binary way, it is both more accurate and more useful to describe expected agent behavior in a probabilistic way.

This insight is already employed in systems ranging from proof-of-stake blockchains to consumer credit scoring and actuarial functions. Agency graphs provide a way for participants to apply this class of insight. Describing behavior probabilistically enables participants to differentiate between *high-certainty* agency and *low-certainty* agency. By working to convert low-certainty personas into high-certainty personas, participants can increase collaboration speed and safety.

Participants can increase certainty in a variety of ways, including increasing authorization minimums, integrating provable attestations, use of verifiable credentials, obtaining confirmations from third party validators and oracles, real-time analysis of connections and endpoints, and incorporation of modular authorization mechanisms.

**System Assertion Scenario: Email Persona Behavior**

| Title | Declaration | Attestation | Verification | Certainty |
|---|:---:|:---:|:---:|---|
| Sender from domain with failed DMARC | ❌ | | | strong negative signal |
| Sender from domain with no DMARC | | | | weak negative signal |
| Sender from domain with compliant DMARC | ✅ | | | weak positive signal |
| DMARC compliant sender from known addresses list | ✅ | ✅ | | strong positive signal |
| DMARC compliant, known sender with GPG key | ✅ | ✅ | ✅ | very strong positive signal |

In general, social personas will have inherently lower fidelity than system personas. System personas are declared by the instantiating platform (the personas' *source of being*). Canonical system persona declarations will have the same level of integrity as the platform. Social personas, however, must be asserted by graph operators, users, or external data sets (such as an HR database) and are subject to data staleness, inconsistency, interpretation, and error. Social persona fidelity is improved through third party attestations, cryptographic verifications, and other quantitative and qualitative mechanisms.

Participants model behavioral certainty to understand access patterns and collaboration risk across arbitrarily large shared resource environments. Participants can use this understanding to reduce risk by adding consensus-oriented control mechanisms to vulnerable portions of the graph. Even small changes in the right place can have a ripple effect that greatly increase expected behavior, and do so without the need for complex role enforcement or aggressive permissions reduction.

---

## Components

### Personas

A **persona** is how we describe agency in digital systems. A persona has three elements: an identifier, the resources the identifier directly controls or embodies, and a set of relationships with other personas.

**(1) an identifier**: a persona must have a locally unique identifier that allows us to reference it within a system.

- *Web1*: `andy@sodal.io` is a unique electronic mail address
- *Web2*: `@andyschwab` is a unique Github user handle
- *Web3*: `0x2dC58F417709323F34653Df24cA1f85bE09d964d` is the unique public key for an Ethereum externally owned account (EOA)
- *Physical*: the author has a recognizably unique, corporeal body in spacetime

**(2) the resources the identifier directly controls or embodies**: a persona is associated with the ability to initiate energy expenditure (to control or consume resources) in its instantiating system.

- *Web1*: The persona associated with `andy@sodal.io` can, through the domain email service provider, send and receive email messages on the public internet
- *Web2*: The persona associated with `@andyschwab` can, through Github's SaaS platform, employ a variety of compute and storage resources for the purpose of managing source code
- *Web3*: The persona associated with `0x2dC58F417709323F34653Df24cA1f85bE09d964d` can, through the Ethereum network, manage resources and exchange those resources for compute
- *Physical*: The persona associated with the author can, through his corporeal form, perform a variety of tasks including reading characters on a computer screen and typing on a keyboard

**(3) a set of relationships with other personas**: a persona is mapped to other personas showing dependent links between those personas. If a persona participates in the agency of another persona, we say it is a controller of that other persona.

The three elements of a persona allow us to map identity recursively as a *composite quality*. We build an increasingly complete understanding of a persona by exploring its controlling personas, the resources it directly controls, and what other personas it participates in.

```mermaid
graph TD
    A[Author<br/>physical persona] --> E["andy@sodal.io<br/>email"]
    A --> G["@andyschwab<br/>GitHub"]
    A --> W["0x2dC5...964d<br/>Ethereum EOA"]
```

The graph above maps the author's persona as the sole controller of each of the other example personas. The activities of the three digital personas are, indeed, part of the author's professional identity and indicate (at least in part) what the author's corporeal self has been busy doing for the last few years.

A **system persona** is a persona defined within and instantiated by a digital system. This definition is broad enough to encompass not only user accounts but groups, teams, channels, documents, repositories, smart contracts, and other capability sets within a digital system.

A **platform** is a *specific* digital system that instantiates and resources personas. Platforms bring actual system personas into being, and no system persona exists apart from an instantiating platform.

There are two system persona subtypes. An **authenticated persona** is directed by one or more credentialled external personas, and serves as the "bridge" between different platforms and platform domains. Conversely, an **internal persona** does not have its own credentials and is acted upon only by other personas in its own platform.

**Persona Types**

| Platform | Type | Subtype | Example Identifier |
|---|---|---|---|
| Email | Account | authenticated | `account@root.tld` |
| Discord | Account | authenticated | `#discordusername1234` |
| Google | Document | internal | `1gkHzjdr1tuMnwNm1fjfc9z8VycSktqTzaoazE2QuKU` |
| Github | Organization | internal | `sodal-project` |
| Slack | Channel | internal | `#team-channel-name` |

A **social persona** is an operator-defined persona that represents people and their relationships to other personas. Social personas attempt to map social and civic constructs within the agency graph: legal personhood, club membership, employment status, team composition, etc.

There are two types of social personas. A **participant persona** represents a human being. An **activity persona** represents a user-defined group of personas, and can include both social and system personas as its controllers.

A composable agency graph combines both social and system personas into a single relationship map. Graph operators use the combined map to create activity personas that incorporate social and system controllers, capturing implicit roles and defining composable collaboration structures. This allows participants to coordinate resources at scale without the need for pre-assigned roles, hierarchies, or other centralized, relational structures.

This is valuable for ad hoc teams that do not have a formal user directory. A Discord server's roles or GitHub organization's membership may function as the de facto source of truth for participation status. An agency graph captures these implicit roles by adding existing system personas as controllers within an aggregate activity persona. The graph operator can now use the activity persona's state to automate alerts or permission assignments across all connected platforms.

### Relationships

Personas form composite identities when operators relate them to other personas. There are two types of relationships in an agency graph: a **controller relationship**, and an **alias relationship**.

A controller relationship describes how personas exercise agency through other personas. A persona is considered a **controller** of an **agent** persona if the controller can access or employ the agent persona's resources, including the resources indirectly influenced by the agent persona through its own controllers.

There are two core properties associated with persona controllers: **access level** and **authorization minimum**. Access level is a controller relationship property that describes a controller's permissions when taking action on behalf of the agent persona. Authorization minimum is a persona property that describes how many controllers must confirm an action before it can take place.

The **authorization minimum** property provides a single attribute to describe a class of related access control mechanisms. These mechanisms all relate to *consensus*: using confirmation from one or more personas to increase confidence that a behavior is expected. Examples of these mechanisms include smart contract multisigning, GitHub branch protection, social media post approval pipelines, threshold cryptography configurations, etc.

**Authorization Minimum**

| Authmin | Meaning | Examples |
|---|---|---|
| **0** | No authentication enforced | Read access in a public chat channel; no-login tools like Pastebin |
| **1** | A single controller must confirm authentication or action | Username and password login; a typical group mailing list where any member can send as the group; a chat channel where every user can post messages |
| **2** | Consensus between two controllers is required for authentication or action | GitHub branch protection with a review requirement prior to merge |
| **N:M** | Consensus between N controllers is required for authentication or action | A multisignature smart contract configured with a 3 of 5 approval structure; a financial approval workflow requiring 3 levels of approval |

Note that agency graphs are not acyclical. It is perfectly possible, for instance, for `abc@example.com` to be a recovery email for the account associated with `xyz@example.com`, and for `xyz@example.com` to be a recovery email for the account associated with `abc@example.com`.

An **alias relationship** allows us to link two distinct personas together as representing the same set of resources and relationships. Many platforms maintain an internal string identifier to reference resources. This immutable string is in addition to the user-defined handle but refers to the same resource. By using system APIs to obtain this internal identifier and then relating user-defined handles as aliases, we can build a more robust and comprehensive graph.

Alias relationships also allow us to model compound platform dependencies. Google Workspace user accounts, for instance, generate associated email addresses linked to the Google persona. In these cases, Google is providing both its own proprietary services and Email platform services through the same agent. The alias relationship captures that these three personas all relate to the same agent, as well as the instantiation dependence the email personas have on the Google persona: when the primary persona ceases to be, the aliases — including the email personas — cease to be as well.

### Assertions

Assertions generate personas and relationships.

Relationships are informed by graph participants as well as graph operators. A participant asserts ownership or access to system accounts by verifying with the graph system that the participant was in control of a given account at a given time. This approach preserves the autonomy of participants in two ways. First, participants are not required to create new, centralized accounts in order to collaborate. Second, assertion activities are voluntary and participant-managed.

By linking multiple accounts to their participant persona, participants increase the fidelity and utility of the graph. Graph operators can incentivize this information sharing by enabling additional capabilities based on verified participant persona attributes.

### Universal Persona Name

The **Universal Persona Name (UPN)** standard describes how persona nodes are named in the graph. UPNs serve as global "primary keys" for all personas. The UPN standard allows independent graph operators to generate consistent, nonconflicting persona identifiers. UPNs also enable graph operators to produce, export, and share independently generated graphs. UPNs should be short, human-readable strings.

> ***The structure outlined here is experimental and subject to frequent change***

A UPN consists of four label components separated by colons. The label components are:

- **UPN**: all UPNs begin with the string `upn` to differentiate them from other string identifiers. It is always lowercase.
- **platform**: the *platform* is the globally unique instantiating system name. Platforms are most easily associated with the commercial activity that maintains the system. It is always lowercase.
- **type**: the *type* is a single-depth, human-friendly way to categorize identifiers within a platform. It is always lowercase.
- **identifier**: the identifier is the locally unique name for the persona. Depending on the platform, identifiers may include additional domain information to ensure the UPN is globally unique. If a system's local identifier is not case sensitive, it should always be lowercase.

**UPN Examples**

| Address Reference | Platform | Type | Identifier |
|---|---|---|---|
| `upn:email:account:andy@sodal.io` | Email | Account | `andy@sodal.io` |
| `upn:github:organization:sodal-project` | Github | Organization | `sodal-project` |
| `upn:github:team:devs@sodal-project` | Github | Team | `devs@sodal-project` |
| `upn:directory:participant:12345` | Directory | Participant | `12345` (an HR-linked identifier) |

---

## Example Use Cases

### Collaborative Access Management

Agency graphs provide a mechanism for robust access management and resource automation in decentralized communities. By decoupling system ownership, resource control, and dependency insights, agency graphs empower every participant to improve how community resources are managed.

### Community Member Lifecycle

Communities manage members through a lifecycle: recruiting, onboarding, role transitions, exits, and the occasional bad actor. Each stage introduces friction when identity is atomic — admitting a new member means manually provisioning access across every platform; a role change means an audit; an exit means hoping no stale access was missed.

Agency graphs let membership state be inferred from relationships rather than enforced from a central directory. A recruit enters at a low authorization minimum and expands as attestations accumulate. Onboarding is the incremental addition of controller relationships. Role transitions are activity persona membership changes. Exits remove controllers without requiring an exhaustive platform-by-platform audit. And when a bad actor surfaces, the graph exposes every resource they can reach — including indirect agency through downstream personas — making containment exhaustive and fast.

### Reputation Management

Participant assertions enable individuals to create and share provable persona agency maps. Graph operators can use insights from these maps and existing agency graph data to establish and refine participant reputation and trust.

### Artificial Intelligence Integration

Agency graphs provide a mechanism to understand and mitigate the risks introduced by artificial intelligence capabilities. The probabilistic output of AI fits naturally into the probabilistic understanding of agency in an agency graph. By incorporating an AI node as simply another persona with dynamic agency, participants can model impact and tune configurations to maintain high net behavioral certainty — maximizing the value of AI while mitigating undesired effects.

### Open Verifiability Framework

Integrating verifiable credentials (VCs) and other cryptographic proving mechanisms into personas can result in both greater behavioral certainty for participants and streamlined interoperability for VC providers.

VCs transition various identity attestations from a siloed, service-centric approach to an ecosystem approach that can give all stakeholders both greater security and flexibility. VCs are themselves atomic, however, and the added complexity of managing the interactions between stakeholders has resulted in high friction and low interoperability in practice.

Agency graphs provide a framework for VC integration that emphasizes their utility while mitigating their drawbacks. VCs can be overlayed on existing personas to increase certainty without requiring participants to migrate to greenfield, stand-alone VC solutions. In this context, VCs don't replace atomic identifiers but instead enhance composite identities.

### Improved Zero Trust

Agency graphs with certainty-based modeling give autonomous participants means to apply NIST 800-207 Zero Trust Framework concepts without centralized policies and controls. Graph operators select composite identity risk priorities based on an independent assessment of workflow criticality and resource sensitivity. Each participant has the freedom to identify what they can control, decide who has access within the context of that control, and select the level of risk they are willing to accept with regard to those resources.

This approach has resilience properties that are inaccessible to strict Zero Trust for this reason: Zero Trust is not actually *zero* trust. Zero Trust shifts trust from the internal enterprise network to the policy engine, assigned atomic identities, and various system dependencies. Each implicit trust anchor represents a risk that Zero Trust cannot directly mitigate.

- *Core Policy Engine*: Because Zero Trust depends on a central policy engine, it is possible for mismanagement or compromise of a single, core policy enforcement system to result in the collapse of the entire security apparatus.
- *System Dependencies*: The Solarwinds supply chain hack illuminated the degree to which centralized Zero Trust often moves liability around rather than addressing the core trust questions. Root certificates, third party integrations, SaaS vendors, and a variety of other dependencies are, once vetted, assumed to be trustworthy. Zero Trust may eliminate "trust and verify" with regard to user access control, but reintroduces it at the level of other (potentially more critical) dependencies.
- *Atomic Identity*: Recent and recurring disclosures of secret and sensitive US Government data illuminate the failure of binary agent behavior mapping in complex systems.
- *Employee & User Trust*: the same technologies that enable ubiquitous centralized control in support of Zero Trust frequently require that employees and users place complete and exhaustive trust in the centralized institution. This is disingenuous, as the risk profile that best protects the organization's board will frequently be at odds with the risk profile that users, employees, or customers consider acceptable.

A certainty-based agency graph approach turns increased community scale into increased resilience by enabling every participant to act as an independent, incentivized threat management node.

### Open Source Supply Chain Verification

Agency graphs provide a mechanism for participants that depend on third party open source software to independently create and maintain behavioral certainty and risk metrics for those dependencies.

Current mitigations — SBOMs, sigstore, provenance attestations — produce useful evidence atomically, without a framework for integrating that evidence into live operational decisions. An agency graph treats each dependency's maintainer set, build pipeline, and release infrastructure as controllers of the published package persona. A package released from a single-maintainer personal account with no branch protection has different behavioral certainty than one released through a multi-signature process with attested provenance. This makes supply chain risk explicit, queryable, and independently assessable by every downstream consumer, without requiring a centralized registry or vetting authority.

### Self-sovereignty

Agency graphs provide a mechanism to unify and bring greater value to existing efforts involving DIDs, Soulbound tokens, and self-sovereignty initiatives. These efforts have produced strong cryptographic primitives but have struggled to find purchase in day-to-day collaboration, partly because they operate at the level of atomic identifiers while real-world trust decisions are made against composite identities informed by relationships and context.

In an agency graph, a DID is not a replacement identity but a high-certainty controller edge. A Soulbound token is an attestation attached to a participant persona, contributing to behavioral certainty without requiring the ecosystem to migrate wholesale to a token-gated paradigm. Participants retain sovereignty over which artifacts they present and to whom; graph operators get a frame for applying those artifacts to live access and risk decisions.

### Collaboration Risk Reduction

Agency graphs show where uncertainty is concentrated in an environment. Increasing certainty has benefits for all stakeholders, and agency graphs can accommodate a variety of mechanisms to increase certainty. Simple mechanisms include programmatic assertions or verifiable credential linking. The concept can be extended further with more complex mechanisms including staking, escrow, and insurance-type control mechanisms.

Participants could, for instance, offset low or non-existent reputation with financial staking or insurance, allowing communities to rapidly incorporate new users and enable greater resource sharing while mitigating the cost of potential abuse. These types of mechanisms may prove particularly valuable to enable fast, safe collaboration in high-privacy contexts, contexts where legal or reputational certainty mechanisms are unworkable or inadequate.

### Systemic Resilience Public Goods

Redundancy is a core aspect of resilience. It is possible, however, for complex systems to appear highly redundant when, in fact, the "redundant" components all share a single, common dependency. In highly decentralized systems, for instance, the value of decentralization may be directly undermined if the majority of participants are drawn to Schelling point infrastructure decisions.

Agency graphs surface these hidden concentrations. Tracing controllers of controllers exposes cases where nominally independent services resolve back to the same cloud provider, root certificate authority, DNS registrar, or upstream package maintainer. This visibility is itself a public good: it lets communities identify single points of failure that no individual participant could see from a local view, and it creates incentives to route around them. Over time, shared agency graph data becomes a map of concentration risk at the level of entire digital ecosystems — the kind of view that individual security audits and compliance frameworks are structurally unable to produce.
