# Sample Output: Expandable Panel Component Review

> **Fictional example:** This sample demonstrates the starter package format. The organizations, sources, findings, and guidance below are invented. They are not product, research, accessibility, or component standards.

## Pilot summary

The Atlas design system team is testing an AI-assisted first review for proposed uses of its expandable-panel component. The pilot should help reviewers catch known issues earlier, cite the guidance behind each finding, and route unresolved product decisions to the right people.

## Workflow brief

| Field | Confirmed answer |
| --- | --- |
| Task | Review a proposed use of the expandable-panel component before design-system approval. |
| Purpose and user outcome | Keep information needed for a customer’s primary decision visible while allowing supporting detail to remain available. |
| Trigger | A product designer submits a panel use through the component-review request. |
| Inputs | Component link, product brief, intended user decision, real content, Atlas panel guidance, implementation reference, and relevant evidence. |
| Current steps | A design-system reviewer inspects the proposal, searches documentation, and asks specialists about gaps. |
| Output | Cited findings, unresolved questions, owners, and next actions. |
| Human decision points | Whether the panel fits the product need, whether an exception is justified, and whether the proposal is approved. |
| AI boundary | The assistant may perform a first review. It may not approve the design, invent missing guidance, or infer implemented behavior from a screenshot. |
| Workflow owner | Morgan Lee, Design System Lead. |
| Approvers | Component owner and product design lead. Specialists confirm findings in their areas. |
| Baseline | The last three reviews averaged 95 minutes and required four follow-up messages. |
| Pilot success | The first pass catches the expected issues in the five test cases, leaves unsupported conclusions unresolved, and reduces review preparation without creating equal correction work. |

## Relevant expertise map

| Area | Contribution to this review | Source | Status |
| --- | --- | --- | --- |
| Design principles | Resolve the tradeoff between compact presentation and decision clarity. | Atlas principle: “Make the next decision clear” | Confirmed |
| Visual language | Define hierarchy, spacing, state treatment, and tokens. | Panel visual specification v2.1 | Confirmed |
| Components | Define supported content, states, and configurations. | Expandable panel usage guide v2.1 | Confirmed |
| Code | Confirm supported behavior and identify implementation checks. | Storybook panel reference v2.1 | Confirmed |
| Information architecture | Guide the label and placement within the page. | Account-page content model | Confirmed |
| Research | Establish which information customers need before opening detail. | Billing comprehension study, May 2026 | Confirmed within the billing context |
| Accessibility | Define design and implementation checks for state and operation. | Atlas panel accessibility checklist | Confirmed |
| Content | Prioritize the amount due, date, and consequence of missing payment. | Billing content standard v3 | Confirmed |

## Source register

| Source | What it helps decide | Owner | Status | Last reviewed |
| --- | --- | --- | --- | --- |
| Product brief: Payment plan eligibility | The customer decision and business rules | Priya Shah, Product | Confirmed | August 18, 2026 |
| Billing comprehension study | Which billing facts must remain visible | Luis Romero, Research | Confirmed for billing flows | May 29, 2026 |
| Billing content standard v3 | Required language and information order | Dana Wu, Content | Confirmed | July 11, 2026 |
| Expandable panel usage guide v2.1 | Supported use and configuration | Morgan Lee, Design Systems | Confirmed | August 2, 2026 |
| Storybook panel reference v2.1 | Implemented properties and behavior | Alex Kim, Engineering | Confirmed | August 2, 2026 |
| Panel accessibility checklist | Interaction and validation requirements | Riley Chen, Accessibility | Confirmed | June 20, 2026 |

## Approved guidance

### Keep payment consequences visible

- **Situation:** A billing flow uses an expandable panel for information related to a payment decision.
- **Decision:** Keep the amount due, due date, and consequence of missing payment visible. Use the panel for supporting explanations and policy detail.
- **Reason:** Participants in the billing study relied on those three facts to decide what action to take. Hiding them delayed or changed the decision.
- **Boundary:** This finding applies to the tested billing flows. Other product areas must confirm which information is necessary for their own primary decision.
- **Acceptable example:** “$120 due September 15. A late fee may apply.” appears beside the payment action. The panel contains fee calculations and policy details.
- **Counterexample:** The page shows only “Payment details,” and the amount, date, and consequence appear after the panel opens.
- **Sources:** Billing comprehension study and Billing content standard v3.
- **Owner:** Dana Wu, Content.
- **Approvers:** Luis Romero, Research; Priya Shah, Product.
- **Status:** Approved for the Atlas billing flow.
- **Affected workflows:** Component review and developer acceptance criteria.

## Reusable AI workflow instruction

Review the proposed expandable panel using the supplied workflow brief and the current sources listed in its source register.

First list the sources you can access and their versions. Identify any required source that is missing. For every finding, identify the affected part of the proposal, cite the governing source, explain the mismatch or uncertainty, and recommend a next action. Separate exact component violations from contextual concerns and decisions requiring human judgment.

Do not approve or modify the component. Do not infer implementation behavior from a screenshot, generalize research beyond the billing context, or invent guidance to fill a gap. Finish with unresolved questions and the named owner or discipline needed to answer each one.

**Human review point:** Morgan checks the full report. Source owners confirm findings in their areas. Priya and the component owner decide whether the proposal proceeds.

## Test plan

| Case | Expected result | Review method |
| --- | --- | --- |
| Supported billing panel with visible amount, date, and consequence | Report no supported issue and avoid filler findings. | AI-assisted first review and human confirmation |
| Unsupported nested panel | Cite the component guidance and identify the unsupported configuration. | Existing component test plus report |
| Approved exception for a regulatory disclosure | Recognize the exception, cite its record, and state its scope. | AI-assisted contextual check |
| Research link unavailable to the reviewer | Leave the visibility conclusion unresolved and route it to Research and Product. | Access check |
| Non-billing proposal using the billing finding | Refuse to generalize the evidence and request relevant product context. | Scope and judgment check |

## Example first-pass result

**Finding:** The proposed design places the amount due and due date inside the closed panel.

**Evidence:** “Keep payment consequences visible,” supported by the Billing comprehension study and Billing content standard v3.

**Recommended action:** Move the amount and due date into the visible summary. Keep calculation details inside the panel.

**Human confirmation:** Product and Content should confirm whether the late-fee consequence applies to this account type. The submitted product brief does not answer that question.

## Shared setup

Atlas uses Confluence for shared guidance, Jira for requests, Figma for component design, Storybook for implementation evidence, and its approved AI assistant for the manual first pass.

- **Confluence:** Start page, workflow brief, source register, approved guidance, workflow instruction, and test results
- **Jira:** Unresolved decisions and requested source changes, linked to the relevant Confluence entry
- **Figma and Storybook:** Authoritative design and implementation evidence
- **AI assistant:** Supplied with the brief and current approved sources during the pilot

The team will consider a tested source connection only after the manual workflow passes its five cases.

## Roles and maintenance

Morgan owns the workflow and reruns affected tests. Each source owner maintains the authoritative material in their system. Priya owns the product outcome and acceptance criteria. The component owner controls design-system approval. Riley confirms accessibility findings that require specialist review.

When the billing content standard changes, Dana updates the authoritative source and creates a linked Jira item. Morgan updates the guidance if needed, refreshes the controlled documents used by the workflow, and reruns the billing cases before the new version is used.

## Open questions and next actions

- Confirm whether the late-fee consequence applies to the submitted account type. Owner: Product.
- Verify keyboard and state behavior in the implemented proposal. Owners: Engineering and Accessibility.
- Confirm that every pilot reviewer can access the current research source. Owner: Workflow owner.

**Smallest useful action today:** Run this proposal against the five test cases with a second reviewer and record the misses and correction time.
