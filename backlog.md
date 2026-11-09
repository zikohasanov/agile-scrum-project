# Product Backlog and Sprint Plan

Priorities are relative and provisional. Work is sliced by customer or staff outcome rather than by document type.

| Order | ID | Backlog item | Value / rationale | Acceptance summary | Dependencies |
|---:|---|---|---|---|---|
| 1 | PBI-01 | View published menu and availability | Lets customer determine what can be requested | Published items show price/options; unavailable items cannot be selected | Menu data and owner policy |
| 2 | PBI-02 | Configure cart and review total | Makes item configuration explicit before submission | Required options, quantity bounds, and price total are validated | PBI-01, tax decision |
| 3 | PBI-03 | Submit request idempotently | Captures a structured request without duplicate retries | One request creates one reference in `AwaitingReview` | Contact channel and retention decision |
| 4 | PBI-04 | Staff accept or reject with reason | Keeps kitchen commitment under staff control | Role-checked decision, required rejection reason, event recorded | PBI-03, staff identity |
| 5 | PBI-05 | Move accepted order through fulfilment | Aligns kitchen and customer order state | Only valid sequential transitions succeed | PBI-04 |
| 6 | PBI-06 | Secure customer status lookup | Reduces status calls while limiting data exposure | Reference plus one-time verification; no details on failure | Verification channel, security review |
| 7 | PBI-07 | Pilot measurement view | Supports a decision about improvement or expansion | Shows agreed counts with baseline and limitations | Metric definitions and event quality |

## Illustrative Sprint 1

**Sprint goal:** A customer can submit a valid pickup request and staff can make an explicit decision.

| Selected work | Sprint outcome | Key risks to surface |
|---|---|---|
| PBI-01 and PBI-02 | Menu and cart rules can be exercised end to end | Tax handling and item-option policy need owner decisions |
| PBI-03 | Valid request creates one pending order reference | Consent wording, contact provider, and retention remain dependencies |
| PBI-04 | Staff can accept or reject a request with an auditable reason | Staff roles and stale-page conflict behavior must be designed |

## Illustrative Sprint 2

**Sprint goal:** An accepted order can be tracked safely through pickup and the team can evaluate pilot learning needs.

| Selected work | Sprint outcome | Key risks to surface |
|---|---|---|
| PBI-05 | Staff can progress order through preparation and collection | Handoff and payment remain in existing restaurant process |
| PBI-06 | Customer can view status after verification | Abuse limits, channel failure, and fallback require review |
| PBI-07 | Owner can inspect proposed pilot measures | Baseline quality and attribution limitations |

This is a planning example, not a report of completed sprints. The product owner and Developers would re-order or re-plan based on discovery and actual capacity.
