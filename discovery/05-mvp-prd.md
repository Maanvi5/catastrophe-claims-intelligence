# MVP PRD

## Product

Catastrophe Claims Intelligence

## Objective

Help catastrophe claims teams prepare for a major weather event and prioritise incoming claims after the event.

## Primary user

Catastrophe claims manager / claims team lead.

---

## MVP User Flow

### Before the event

1. User selects an upcoming weather event.
2. User sees the expected event severity and affected geography.
3. User sees insured exposure in the affected area.
4. User sees expected claims volume and severity.
5. User identifies areas where additional claims capacity may be required.

### After the event

1. User switches to the event's actual impact.
2. Claims begin appearing in the claims queue.
3. User filters and sorts claims.
4. User selects a claim.
5. User sees claim, property and environmental context.
6. Product suggests a handling path.
7. User reviews the supporting evidence.
8. User accepts, changes or flags the recommendation.

---

## Prepare View

### Inputs

- Weather event
- Event location
- Event severity
- Event timing
- Insured property locations
- Property / asset information

### Outputs

- Potentially affected properties
- Exposure by geography
- Expected claims volume
- Expected severity
- Areas requiring additional attention

### Primary decision

> Where should the claims team prepare additional capacity?

---

## Triage View

### Inputs

#### Claim

- Claim ID
- Claim amount
- Reported damage
- Damage severity
- Claim date

#### Property

- Location
- Asset type
- Property value / exposure

#### Environmental

- Event type
- Event severity
- Local environmental impact
- Distance / relationship to event footprint

#### Evidence

- Photos / documentation availability
- Remote assessment availability

### Outputs

- Claim priority
- Recommended handling path
- Reasons supporting the recommendation

### Primary decision

> What level of assessment does this claim need?

---

## Handling Paths

### Remote review

Use when available evidence is sufficient for initial assessment.

### Desk assessment

Use when the claim needs human review but may not require a field visit.

### Field assessment

Use when physical inspection is likely to be important.

### Specialist review

Use when the claim requires additional expertise or investigation.

---

## Key Screens

### 1. Event Overview

Shows:

- Event status
- Severity
- Affected geography
- Exposed properties
- Expected / actual claims
- Key summary metrics

### 2. Claims Queue

Shows:

- Claim ID
- Location
- Claim amount
- Asset type
- Severity
- Priority
- Recommended handling path

Supports filtering and sorting.

### 3. Claim Detail

Shows:

- Claim information
- Property information
- Event information
- Environmental context
- Available evidence
- Recommended handling path
- Reason for recommendation

---

## Recommendation Logic

The MVP will use transparent rules rather than a black-box model.

Example factors:

- Event severity
- Damage severity
- Claim amount
- Asset type
- Available evidence
- Property exposure

The recommendation should always show why it was made.

Example:

> **Field assessment**
>
> Severe flood impact + high reported damage + insufficient remote evidence.

The user can override the recommendation.

---

## Data

The prototype will use synthetic claims and event data.

Target dataset:

**20,000 synthetic claims**

The data should allow us to simulate a major catastrophe and test the workflow at realistic volume.

---

## Success Metrics

### Primary

- Time required to identify high-priority claims
- Time required to determine a handling path

### Secondary

- Percentage of claims routed without unnecessary escalation
- User agreement with recommendations
- Percentage of recommendations overridden

### Product question

> Does bringing claim, property and environmental context together make the handling decision faster or clearer?

---

## Out of Scope

- Automated claim approval
- Automated settlement
- Fraud detection
- IBNR forecasting
- New weather forecasting models
- Full catastrophe modelling
- Production insurer integrations
- Real claims data

---

## MVP Success

The prototype is successful if a user can move from:

**Event → exposure → claims → evidence → handling decision**

within one workflow, without needing to manually combine multiple data sources.
