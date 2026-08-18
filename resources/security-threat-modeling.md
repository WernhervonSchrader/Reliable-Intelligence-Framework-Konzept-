# RIF / Decision Assurance Resources — Security & Threat Modeling

**Status:** Curated resource note  
**Added:** 18 August 2026  
**Scope:** Security, threat modeling, agentic systems, Decision Assurance

## Purpose

These sources support the security and threat-modeling perspective around the Reliable Intelligence Framework (RIF) and Decision Assurance (DA). They are not treated as interchangeable authorities. Each contributes a different layer to the analysis of model capability, application authority, trust boundaries, evidence, controls, and operational effects.

## Sources and relevance

### 1. Cloud Security Alliance — MAESTRO

**Source:** https://cloudsecurityalliance.org/blog/2025/02/06/agentic-ai-threat-modeling-framework-maestro

**Role:** Agentic architecture, trust boundaries, cross-layer threats, and multi-agent risk.

**RIF / DA relevance:** Particularly useful where models interact with retrieval, memory, tools, identities, infrastructure, or other agents. MAESTRO helps identify where threats originate and how they propagate across layers. For Decision Assurance, this supports explicit authority boundaries and the separation of model output from execution authority.

**Related concepts:** Actor Independence; authority boundaries; runtime controls; tool and agent governance.

### 2. OWASP GenAI Security Project

**Source:** https://owasp.org/www-project-top-10-for-large-language-model-applications/

**Role:** Concrete GenAI attack and failure patterns, including prompt injection, excessive agency, insecure output handling, sensitive information disclosure, and tool-related risks.

**RIF / DA relevance:** Useful as an adversarial source for control design, failure classes, test cases, and benchmark scenarios. It helps translate known GenAI risks into deterministic gates and assurance requirements outside the model.

**Related concepts:** Deterministic gates; benchmark regression; input/output controls; tool authorization.

### 3. MITRE ATLAS

**Source:** https://atlas.mitre.org/

**Role:** Adversarial tactics, techniques, attack paths, observable behavior, detection, and telemetry for AI-enabled systems.

**RIF / DA relevance:** Supports the connection between attack hypotheses and observable evidence. Particularly relevant to auditability, runtime observability, adversarial testing, and reconstruction of security-relevant events.

**Related concepts:** Evidence chains; telemetry; append-only audit; observability; adversarial testing.

### 4. NIST AI Risk Management Framework

**Source:** https://www.nist.gov/itl/ai-risk-management-framework

**Role:** Governance and risk-management framework structured around Govern, Map, Measure, and Manage.

**RIF / DA relevance:** Provides a broader governance context for Decision Assurance and helps connect technical assurance mechanisms with organizational accountability, measurement, and risk treatment. DA can provide concrete decision-level mechanisms beneath this broader governance layer.

**Related concepts:** Governance; accountability; assurance measurement; human oversight; risk management.

### 5. Microsoft Threat Modeling Tool / STRIDE

**Source:** https://learn.microsoft.com/en-us/azure/security/develop/threat-modeling-tool

**Role:** Classical threat modeling of components, data flows, trust boundaries, and enforcement points using approaches such as STRIDE.

**RIF / DA relevance:** Provides a technology-independent architectural discipline that complements AI-specific frameworks. It is particularly useful for identifying where deterministic controls must be enforced rather than relying on probabilistic model behavior.

**Related concepts:** Trust boundaries; deterministic enforcement; data flows; identity; authorization.

## Synthesis for RIF / Decision Assurance

A common conclusion across these resources is that security does not emerge from the model alone. Critical behavior must be controlled across trust boundaries, identities, data, policies, tools, infrastructure, and operational effects.

Decision Assurance adds a complementary question to conventional threat modeling:

> **Threat Modeling asks where a decision or action can be attacked, manipulated, or lose control. Decision Assurance additionally asks whether the concrete decision is supported by appropriate evidence, compliant with applicable rules, authorized, and independently reconstructable and verifiable.**

This leads to a useful architectural chain for consequential decisions:

**Model Output → Deterministic Rules / Policies → Independent Evidence → Authorized Decision → Traceable Effect**

The sources in this collection therefore support RIF / DA work on:

- Actor Independence
- deterministic gates
- evidence chains and provenance
- authority boundaries
- runtime controls
- auditability and observability
- adversarial benchmarks
- governance and human accountability

## Classification

**Resource category:** Security / Threat Modeling / Agentic Systems  
**Use in RIF:** Architecture, threat analysis, control design, benchmark design  
**Use in Decision Assurance:** Authority separation, deterministic enforcement, evidence verification, runtime assurance and traceability
