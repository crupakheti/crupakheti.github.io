---
layout: post
author: Chandan Rupakheti
description: Architectural Decision Records (ADR) - What, Why, and How
last_modified_at: 2021-06-05
comments: true
tags: Architecture, Documentation
---

As an engineer/architect, we make many important design decisions. Most of these decision are made in the context of available tools and constraints. As things evolve and as new features are solutioned, we may need to re-evaluate, redsign, refactor, or extend existing systems. If the key drivers for an architecturally significant decision are not adequately documented, we may need to spend a good chunk of time figuring out the rantionale for those design decisions before taking any further steps.

We have recently started documenting architecturally significant decisions for a large-scale customer portal at a client using a customized [ADR](https://adr.github.io/) template. Here is our approach:

1. We started a Git repo in the company's internal Git server.
2. We created a folder each for portal's microservices in the repo to document micro-service-specific decisions. Typically these decisions affect the quaility attributes such as availability, performance, and security of the dependent micro-services.
3. We created a `global` folder for the decisions that would impact the entire system, i.e., majority of micro-services.
4. We made educated effort to produce concise documentation that had enough information for an engineer/architect to decipher the rationale for the decisions about the portal/microservices. We used the following Markdown Template:

## ADR Custom Markdown Template
<pre>
# [A Meaningful Title]

* Status: [proposed | rejected | accepted | deprecated]
* Members: [Members involved in the decision]
* Date: [Date when the ADR was last modified]
 
## Context

[Describe the problem and key drivers. Use architecture diagrams when applicable]

## Solution

### Option 1
[Description - use diagrams when applicable]

### Pros
- [Talk about how the solution helps]

### Cons
- [Talk about limitations]

### Option 2
[Description - use diagrams when applicable]

### Pros
- [Talk about how the solution helps]

### Cons
- [Talk about limitations]

## Decision
Talk about which options was finally chosen and why.
</pre>

## Further Reading

Here are some resources that we looked at before ariving at our current approach:

1. [J. Henderson's Github Repo](https://github.com/joelparkerhenderson/architecture-decision-record)
2. [ADR GitHub Org](https://adr.github.io/)
3. [ThoughtWorks Technology Radar Recommendation](https://www.thoughtworks.com/radar/techniques/lightweight-architecture-decision-records)
