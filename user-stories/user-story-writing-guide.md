# ProQuest User Story Writing Guide

## Purpose

This guide ensures user stories:

- Clearly describe business intent
- Are aligned to Statement of Work (SOW) scope
- Are testable and implementation-ready
- Minimise ambiguity for consultants and clients
- Support clean acceptance criteria creation

---

# 1. Core User Story Structure

All stories must follow:

AS A [persona]  
I WANT TO [action or capability]  
SO THAT [business value or outcome]

---

# 2. How to Write High-Quality User Stories

## 2.1 Persona Must Be Real and Specific

Avoid:
- “User”
- “System”
- “Salesforce”

Use:
- Scheduler
- Field Technician
- Service Manager
- Marketing Manager
- Customer
- Finance Administrator

The persona must reflect an actual business role.

---

## 2.2 The Action Must Describe Capability, Not Configuration

Avoid:
- “Create a flow”
- “Add a validation rule”
- “Update a field”

Use:
- “Prevent bookings outside SLA windows”
- “Optimise daily routes before dispatch”
- “Automatically notify customers when status changes”

Focus on behaviour and outcome.

---

## 2.3 The Business Value Must Be Measurable or Strategic

Avoid vague benefits:
- “So that it works better”
- “So that we improve things”

Use:
- “So that travel time is reduced”
- “So that SLA breaches are minimised”
- “So that reporting accuracy improves”
- “So that manual admin effort is reduced”

Every story must justify why it exists.

---

# 3. Definition of Ready (DoR)

A story is ready for development when:

- Persona is clearly defined
- Business value is articulated
- Scope alignment is confirmed
- Dependencies are identified
- Scheduling constraints are documented (if relevant)
- Edge cases are identified
- Acceptance criteria can be written clearly

If these are missing, the story is not ready.

---

# 4. Definition of Done (DoD)

A story is complete when:

- All acceptance criteria pass
- Negative scenarios are validated
- Permissions are verified
- Reporting impact is tested
- No regression issues are introduced
- Client confirms behaviour meets expectations

---

# 5. When to Split a User Story

Split a story when:

- Multiple personas are involved
- Multiple independent behaviours exist
- Different business outcomes are targeted
- Story becomes too large to estimate confidently

Rule of thumb:
If it cannot be delivered within one sprint, split it.

---

# 6. Behaviour vs Technical Stories

### Preferred: Behaviour-Focused

AS A Scheduler  
I WANT TO optimise appointment routes  
SO THAT total daily travel time is reduced

### Avoid: Technical-Focused

AS A Developer  
I WANT TO configure optimisation rules  
SO THAT the system works

Technical tasks should be implementation subtasks, not primary user stories.

---

# 7. Handling Edge Cases

Every story must consider:

- What happens if required data is missing?
- What happens if permissions are insufficient?
- What happens if SLA windows conflict?
- What happens if optimisation cannot find a solution?

Edge case handling may require separate acceptance criteria.

---

# 8. Field Service Specific Considerations

For Field Service projects, stories must consider:

- Travel time vs service window trade-offs
- Resource skills and territory constraints
- Emergency job prioritisation
- Manual override scenarios
- Optimisation timing (before dispatch vs real-time)
- Appointment Assistant behaviour
- Team leader usage rules

Scheduling and optimisation constraints must be explicitly documented.

---

# 9. Linking to Scope

Each story must include:

- SOW reference ID (if applicable)
- Workshop source reference
- Business priority (High / Medium / Low)
- Impacted objects or features (high-level only)

Example metadata section:

---

## Metadata

- SOW Reference: FSL-OPT-01
- Priority: High
- Workshop Date: 11 Feb 2026
- Module: Field Service Scheduling

---

# 10. Writing Anti-Patterns to Avoid

Do not:

- Combine multiple unrelated capabilities
- Write stories without business value
- Hide technical assumptions inside story text
- Use ambiguous language like “should” or “maybe”
- Leave performance expectations undefined

---

# 11. Good vs Poor Example

### Poor

AS A Scheduler  
I WANT the system to be better  
SO THAT everything works

---

### Strong

AS A Scheduler  
I WANT appointment schedules optimised before dispatch  
SO THAT daily travel time is reduced while maintaining SLA compliance

---

# 12. Estimation Guidance

Stories should be:

- Clear enough to estimate confidently
- Small enough to deliver in a sprint
- Independent where possible
- Not blocked by unknown discovery

If unknowns exist, create a spike story.

---

# 13. AI Usage Standard

When generating stories using AI:

- Always align to this document
- Validate persona accuracy
- Confirm business value is real
- Remove technical implementation detail
- Ensure story could be explained to a non-technical client

AI output must be reviewed before client exposure.

---

# 14. Checklist Before Finalising a Story

- [ ] Persona is realistic and specific
- [ ] Action describes behaviour
- [ ] Business value is clear
- [ ] Scope alignment confirmed
- [ ] Acceptance criteria can be written
- [ ] Edge cases considered
- [ ] No hidden technical bias

---

# 15. Maturity Standard

ProQuest user stories should:

- Be client-ready
- Be audit-ready
- Be reusable as templates
- Reflect consulting-grade clarity
