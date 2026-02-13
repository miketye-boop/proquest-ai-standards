# Guide: Writing Strong Given–When–Then Acceptance Criteria

## 1. Purpose of Acceptance Criteria

Acceptance criteria define **how we know a user story is complete and working correctly**.

They:

- Clarify expected system behaviour  
- Remove ambiguity  
- Create alignment between business, consultant, and developer  
- Translate directly into test scenarios  
- Prevent scope creep  

Acceptance criteria describe **observable behaviour**, not implementation.

---

## 2. The Given–When–Then Structure

Each scenario follows this structure:

### Given  
The starting context or precondition.

### When  
The action or event that occurs.

### Then  
The expected outcome or result.

---

### Example

User Story:  
_As a Scheduler, I want to minimise travel time when booking appointments so that daily schedules are more efficient._

Acceptance Criteria:

- **Given** I am booking a Service Appointment  
- **When** I search for available time slots  
- **Then** the system displays available resources ordered by lowest travel time  

---

## 3. What Acceptance Criteria Should Focus On

### ✔ Behaviour-focused  
Describe what the system does from the outside.

### ✔ User or business outcome  
Use persona language (Scheduler, Assessor, Client, Administrator).

### ✔ Observable and testable  
Someone should be able to validate the result without knowing how it was built.

### ✔ One behaviour per scenario  
Avoid combining multiple outcomes into one Then statement.

---

## 4. What to Avoid

### ✘ Technical implementation details  
Do not reference:

- Flow names  
- Apex classes  
- SOQL  
- Object schema  
- Metadata configuration  

Bad example:
> Given the Flow is triggered  
> When the record updates  
> Then the SOQL query retrieves ServiceResource records  

This describes *how* it is built, not what the user experiences.

---

### ✘ Vague language

Avoid phrases like:

- “Works correctly”  
- “System behaves as expected”  
- “Optimises efficiently”  

Instead, be specific and measurable.

---

## 5. Writing Measurable Criteria

Where possible, include quantifiable outcomes.

Example:

- **Then** the appointment is scheduled within the technician’s operating hours  
- **Then** travel time between consecutive appointments does not exceed 30 minutes  
- **Then** the system sends confirmation within 2 minutes  

If it cannot be tested, it is not strong acceptance criteria.

---

## 6. Functional vs Technical Stories

### Functional Story (Most Common)

Primary focus → User behaviour  
Secondary focus → Business value  
Never primary → Technical design  

### Technical Story (Rare)

If the story is explicitly technical (e.g. “As a Developer…”), technical validation is acceptable.

---

## 7. Quality Checklist

Before finalising acceptance criteria, check:

- Does it describe behaviour, not implementation?
- Is it written in persona or business language?
- Is it testable?
- Is it measurable where appropriate?
- Would it remain valid if the build approach changed?

If the answer to all five is yes, the criteria are strong.

---

## 8. Common Mistakes

| Mistake | Why It’s Wrong |
|----------|----------------|
| Writing steps instead of behaviour | Describes process, not outcome |
| Combining multiple scenarios | Makes testing unclear |
| Referring to system internals | Locks criteria to a specific build method |
| Leaving edge cases undefined | Creates ambiguity |

---

## 9. Advanced Tip

For complex behaviour, write multiple scenarios:

- Happy path  
- Edge case  
- Validation failure  
- Exception handling  

Each should have its own Given–When–Then block.

---

## 10. Final Rule

Acceptance criteria should answer:

> “How will we know this works — from the outside?”

Not:

> “How are we building it?”
