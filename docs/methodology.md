# Generation and quality methodology

Req2Test AI combines transparent deterministic rules with optional Azure OpenAI augmentation. AI output is always draft material.

## Evidence thread

`Requirement → Quality issues → Generated tests → Traceability → Duplicate review → Human disposition → Export`

## Requirement quality checks

The MVP detects vague wording, absolute claims, missing normative language, missing conditions, absent quantitative thresholds for performance requirements, compound length, and incomplete sentence structure. Scores are triage indicators, not compliance ratings.

## Deterministic generation

Every requirement generates positive, negative, and robustness tests. Quantified thresholds generate below/at/above boundary cases. Performance requirements add timing tests. Safety-relevant requirements add fault-response tests. Cybersecurity-relevant requirements add unauthorised, malformed, and replay scenarios.

## AI augmentation

When Azure OpenAI is configured and explicitly selected, it may add at most three draft, non-duplicate scenarios. Provenance records the model deployment. The deterministic suite remains present, and a human reviewer must approve every test.

## Production backlog

1. Entra/OIDC authentication, RBAC, tenant isolation, and signed audit events.
2. PostgreSQL/Azure SQL and versioned requirement baselines.
3. ReqIF, DOORS, Polarion, Jama, Azure DevOps, and Jira import/export.
4. Domain ontology, parameter extraction, pairwise/combinatorial generation, and state-transition models.
5. Semantic duplicate detection with an approved embedding model and explainable thresholds.
6. Test execution integrations and coverage feedback from SIL/HIL/vehicle environments.
7. Configurable OEM quality policies, review matrices, and electronic signatures.
8. Signed PDF/CSV evidence packs and integrations with Vehicle API Lab, VariantGuard, CyberEvidence, and OTA Evidence Hub.
