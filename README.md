# H-SDACLP (SDALP)

Human-in-the-Loop Software Development Agent Continuous Lifecycle Protocol.

- Formal name: H-SDACLP
- Operational name: SDALP
- Pronunciation: sdalp /sdælp/
- Version: H-SDACLP/1.0
- Status: FINAL (HARD LOCK - SOC CLEAN)

## Abstract

H-SDACLP defines a protocol for orchestrating software development agents in a continuous, closed-loop lifecycle. It enforces strict separation of concerns across lifecycle execution, data modeling, storage, observability, and governance to ensure auditability, reproducibility, and human-in-the-loop decision control.

## Core Lifecycle Loop

CE -> CV -> CC -> CL -> CO
-> CP
-> CUS -> CES -> CMS
-> CRFC -> CS
-> CB -> CT -> CUTC -> CQC -> CQA -> CR -> CUAT -> CUBS
-> CI -> CD
-> CLog -> CTrace -> CMetric -> CAlert -> CMonitor -> CHealth -> CReady -> CReport
-> CAR -> CAG -> CAC -> CAD -> CA
-> CM -> CF -> CX -> CK -> CBC
-> RB -> CE

## Phase Groups

### Economic

- CE: Continuous Exploration
- CV: Continuous Value
- CC: Continuous Cost
- CL: Continuous Leverage
- CO: Continuous Optimization

### Product

- CP: Continuous Product

### Story

- CUS: Continuous User Story
- CES: Continuous Enabler Story
- CMS: Continuous Mediator Story (HUMAN-ONLY)

### Protocol

- CRFC: Continuous RFC
- CS: Continuous Specification

### Engineering

- CB: Continuous Build
- CT: Continuous Test
- CUTC: Continuous Unit Test Coverage
- CQC: Continuous Quality Control
- CQA: Continuous Quality Assurance
- CR: Continuous Refactor
- CUAT: Continuous User Acceptance Testing
- CUBS: Continuous User Behavior Simulation
- CI: Continuous Integration
- CD: Continuous Deployment

### Observability (Signal Layer)

- CLog: Continuous Logging
- CTrace: Continuous Tracing
- CMetric: Continuous Metrics
- CAlert: Continuous Alerting
- CMonitor: Continuous Monitoring
- CHealth: Continuous Health
- CReady: Continuous Readiness
- CReport: Continuous Reporting

### Governance (Decision Layer)

- CAR: Continuous Assess for Release
- CAG: Continuous Assess Gate
- CAC: Continuous Approval Compliance
- CAD: Continuous Approval Decision (HUMAN)
- CA: Continuous Approval (HUMAN)

### Business

- CM: Continuous Monetization
- CF: Continuous Funding
- CX: Continuous Experience
- CK: Continuous Kill / Pivot
- CBC: Continuous Competition

### Recovery

- RB: Continuous Rollback

## Global Invariants

### CVersion

- All artifacts must be versioned.
- Append-only.
- Full lineage traceable.

### CRevision

- All changes must be revision-tracked.
- Must include actor, timestamp, and diff.
- Full history reconstructable.

## Design Principles

- HITL: Human-required phases are CMS, CAD, and CA.
- SoC: One phase equals one agent. No shared state. No cross-phase mutation.
- RACI: Every phase must define R/A/C/I.
- C<name> extensibility: Each extension defines doc, spec, RFC, agent, environment, deployment, development, and definition.
- MA (Minimal Adoption): Subset adoption is allowed if core invariants remain preserved.

## Agent Model

- One phase equals one agent.
- Stateless execution.
- Communication via artifacts and events only.
- Human-only phases: CMS, CAD, CA.

## Execution Modes

- Pipeline: linear
- Graph: DAG
- Vector: optimization
- Geo: distributed

## Quality and Governance Chains

- Quality: CT -> CUTC -> CQC -> CQA -> CUAT -> CUBS
- Governance: CD -> CAR -> CAG -> CAC -> CAD -> CA -> CM

System-controlled governance phases: CAR, CAG, CAC.
Human-controlled governance phases: CAD, CA.

## Failure and Recovery

- Test failure: CT -> CQC -> CR -> CT
- Deployment failure: CD -> RB -> CR -> CI -> CD

## Repository Layout

- docs/: protocol documentation and phase documentation
- specs/: governance and invariant specifications
- reference/: architecture and flow references
- examples/: adoption blueprints
- implementations/: sample implementation and integration stubs

## Source of Truth

Primary canonical specification is maintained in H-SDACLP.txt.

## Compliance Requirements

Implementations must:

- Enforce SoC.
- Enforce HITL.
- Enforce governance chain.
- Implement observability.
- Support rollback.
- Maintain lineage.
- Enforce CVersion and CRevision.
