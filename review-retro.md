# Sprint Review, Retrospective, and Metrics

## Review prompts

1. Can a customer distinguish “request received” from “restaurant accepted”?
2. Can staff find and decide the oldest pending request without seeing unnecessary contact data?
3. What happens when availability changes, a staff page is stale, or notification delivery fails?
4. Which operational policies remain undecided before a pilot?
5. What feedback changes the backlog order?

An increment should be reviewed in its working form. Stakeholder feedback informs the backlog; it is not automatically a release approval.

## Retrospective format

Use **Keep / Change / Try**. Ask each participant to cite a specific event or observation, then choose one small experiment with an owner and a check date.

| Example observation (simulation) | Experiment | Evidence to inspect |
|---|---|---|
| Menu availability is a dependency for meaningful checkout examples | Ask the owner role to confirm who updates availability and when | Decision recorded; test data covers unavailable item |
| Notification behavior can hide an otherwise persisted order | Add delivery-failure acceptance example and staff-visible retry state | Scenario demonstrated without claiming external delivery reliability |

These are sample prompts, not claims that a retrospective occurred.

## Metrics and responsible interpretation

- **Outcome:** corrections per 100 orders attributable to re-entry, compared with a documented baseline.
- **Outcome:** status-check calls per 100 pickup orders, with customer channel and opening hours recorded.
- **Flow:** time from order submission to staff decision, segmented by accepted/rejected and time of day.
- **Quality:** duplicate-order rate, invalid transition attempts, and notification failures.

Do not use story points as an individual performance measure. Do not claim the product caused outcome changes from a simple before/after comparison; document confounders and sample size.
