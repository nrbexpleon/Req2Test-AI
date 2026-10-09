# Req2Test AI

Human-reviewed requirements-to-test engineering for automotive software.

Req2Test AI helps engineering and quality teams assess requirement quality, generate structured positive/negative/boundary/robustness tests, maintain bidirectional traceability, detect duplicates, and route every generated test through accountable review.

## MVP capabilities

- Requirement-set and programme context
- Requirement quality linting for ambiguity, unverifiable wording, missing conditions, units, timing, and acceptance criteria
- Deterministic test generation for positive, negative, boundary, robustness, timing, and cybersecurity-relevant scenarios
- Optional Azure OpenAI augmentation behind explicit configuration
- Generated-test provenance and requirement traceability
- Similarity-based duplicate detection
- Human approval, rework, rejection, and editing workflow
- Coverage and evidence-gap dashboard
- JSON/CSV export and append-style audit history
- REST API, responsive UI, tests, Docker, and Azure deployment assets

## Important limitation

AI and rule-based generation provide draft engineering assets only. Generated tests can be incomplete or incorrect and must be reviewed by competent engineers. The tool does not certify ASPICE, ISO 26262, ISO/SAE 21434, or product compliance.

## Run

Requires Node.js 20+.

```bash
npm test
npm start
```

Open http://localhost:3000.

Azure OpenAI is optional. Without it, the complete deterministic workflow remains available.

## API

- `GET /api/health`
- `GET|POST /api/projects`
- `GET /api/projects/:id`
- `POST /api/projects/:id/requirements`
- `POST /api/projects/:id/generate`
- `POST /api/projects/:id/tests`
- `POST /api/projects/:id/reviews`
- `GET /api/projects/:id/report`
- `GET /api/projects/:id/export.csv`

See `docs/methodology.md` for the generation and quality model.
