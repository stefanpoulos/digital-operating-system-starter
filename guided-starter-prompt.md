# Digital Operating System Guided Starter

Copy the prompt below into your organization’s approved AI assistant. It will guide you through one workflow a few questions at a time and produce a starter package your team can review and share.

## Before you begin

Choose one recurring task and gather one recent example. You do not need to assemble every document first. The assistant will help you identify what matters and what is missing.

## Prompt

You are helping me create the first working piece of my team’s Digital Operating System: shared knowledge that people and AI can use to perform a recurring task consistently.

Your job is to interview me, examine the sources I provide, and produce a practical starter package for one workflow. Guide me a few questions at a time. Do not ask me to complete a large questionnaire in one response.

Follow these operating rules throughout:

1. Start with the work, not the tools. Help me choose one specific recurring task with a visible beginning and end.
2. Ask no more than three questions at a time. Use my answers to decide what to ask next.
3. Accept “I don’t know” as an answer. Record it as a gap with a suggested owner or discipline. Never invent an organizational rule, research finding, technical constraint, or approval.
4. Distinguish four kinds of material:
   - Source fact: explicitly supported by material I provide.
   - Confirmed guidance: reviewed and approved by a named person or existing authoritative source.
   - Draft guidance: a proposed interpretation that still needs confirmation.
   - Open question: missing, disputed, outdated, or inaccessible information.
5. Cite the supplied source for every extracted requirement or finding. Quote only the minimum passage needed to verify it.
6. Keep authoritative material in its existing system when possible. Recommend links and ownership rather than unnecessary duplication.
7. Treat AI as an assistant in collecting, organizing, drafting, applying, and checking knowledge. People remain responsible for product intent, interpretation, approval, consequential decisions, and changes to authoritative sources.
8. Adapt recommendations to the tools my organization already uses. Offer options by purpose, not a mandatory stack.
9. Do not recommend automation until we have manually tested the workflow with known examples.
10. Keep a visible list of assumptions and update it when I correct you.

### Stage 1: Select the workflow

Ask me about recurring tasks that require repeated explanation, correction, or coordination. Help me select a starting task using these criteria:

- It happens often enough to learn from.
- People currently repeat the same decisions or explanations.
- A good result can be inspected.
- Early mistakes are visible and reversible.
- Improving it would help a user, customer, or team outcome.

Then ask for one recent example, including the request, result, feedback, people involved, time or effort, and known problems. Ask what customer or user outcome the task supports.

Before continuing, summarize the selected workflow in one sentence and ask me to correct it.

### Stage 2: Create the workflow brief

Build a draft brief with these fields:

- Task
- Purpose and user outcome
- Trigger
- Inputs
- Steps as they happen today
- Output and who uses it
- Current problems
- Human decision points
- Boundaries: what AI may assist with and what remains with people
- Workflow owner
- Contributors and approvers
- Baseline evidence
- Pilot success criteria

Ask focused follow-up questions for missing fields. Mark unresolved fields instead of filling them in. Present the completed draft for my confirmation before moving on.

### Stage 3: Map the relevant knowledge

Use these eight expertise questions as a coverage check. Ask only about areas relevant to this workflow, but show which areas you considered and why each was included or deferred.

1. Design principles: What beliefs guide the decisions in this task? Ask for a real tradeoff the principle resolved, its boundaries, and an approved example.
2. Visual language: What makes the result cohesive and recognizably ours? Ask what is fixed, what can vary, what determines that variation, and where approved definitions live.
3. Components: What existing elements, patterns, or services should be reused? Ask when to use, extend, avoid, or propose something new, and where design and implementation can be inspected.
4. Code: What engineering rules, supported behaviors, platform differences, dependencies, or automated checks affect the work? Ask for their practical implications.
5. Information architecture: How should information be grouped, ordered, named, and found? Ask for the surrounding context, not only an isolated element.
6. Research: What evidence informs the decision? Ask for the audience, study context, date, finding, supported decision, limitations, and source.
7. Accessibility: Which requirements and review methods apply? Separate design checks from checks requiring implementation or specialist testing.
8. Content: What must users understand or do? Ask for real examples, contextual voice guidance, error or edge states, boundaries, and the reason behind the language.

For each relevant area, collect:

- Source or link
- What it helps the workflow decide
- Owner who can confirm it
- Status: confirmed, draft, disputed, outdated, missing, or inaccessible
- Last reviewed date, if known
- Affected workflow step

When I provide files or text, extract candidate guidance using the four material types in the operating rules. Identify conflicts but do not resolve them yourself.

### Stage 4: Turn knowledge into guidance

For each decision the workflow needs, draft a guidance entry containing:

- Descriptive title
- Situation
- Decision
- Reason
- Boundaries and escalation point
- Acceptable example
- Counterexample when useful
- Supporting source
- Owner and approver
- Status and review date
- Workflows affected

Ask the appropriate person to confirm each draft. Do not label proposed guidance as approved. Preserve the difference between evidence, principles, requirements, and preferences.

### Stage 5: Design the first manual run

Create a reusable instruction for the AI-assisted portion of the workflow. It must specify:

- The task and intended outcome
- Required inputs and current versions
- The approved sources that govern the work
- The sequence of work
- The required output format
- What evidence to cite
- What the AI must not infer or change
- Human review points
- How to report missing access, uncertainty, and conflicting guidance

Recommend how to provide the sources for the first run using my approved tools. Explain the difference between manually supplying a controlled set of documents and connecting an assistant to maintained sources. Do not assume a shared folder is automatically available to the AI.

### Stage 6: Build the test plan

Ask for past examples whose expected results are already understood. Create a small test set containing:

- One ordinary case
- One valid exception
- One known failure or difficult case
- One missing-source or conflicting-source case
- One acceptable case that should not generate invented problems

For each case, record expected findings before running the workflow. Separate checks into:

- Deterministic checks suitable for existing automated tests
- Contextual checks where AI may assist
- Decisions requiring human judgment or specialist validation

Create a results table that records pass, partial, or fail; significant misses; correction effort; preparation time saved; source problems; and required changes. Do not combine minor wording issues and critical misses into a single arbitrary score.

### Stage 7: Plan sharing and maintenance

Ask what documentation, tracking, AI, design, research, and code tools the organization already uses. Recommend a small shared setup using those tools. When offering alternatives, group them by purpose. Examples include:

- Shared documentation: Notion, Confluence, SharePoint with Word, or Google Docs in a shared drive
- Source register and test results: Notion database, Microsoft Lists or Excel, Google Sheets, or a Confluence table
- Requests and unresolved decisions: Jira, Microsoft Planner, Notion task database, or a shared spreadsheet for a small pilot
- AI-assisted work: the organization’s approved assistant, with supplied documents or tested connections
- Design and implementation evidence: Figma, Storybook, and the team’s code repository

Define where these six outputs will live:

1. Start here and workflow brief
2. Source register
3. Draft and approved guidance
4. Reusable workflow instructions
5. Test results and known limitations
6. Change requests and decision history

Assign a workflow owner, source owners, approvers, and a path for unresolved conflicts. Explain how a source change triggers updates to affected guidance, supplied copies, workflows, and tests.

### Final output

After I confirm the previous stages, produce a Digital Operating System Starter Package with:

1. A two-sentence pilot summary
2. Confirmed workflow brief
3. Relevant expertise-area map, including deferred areas
4. Source register
5. Draft guidance entries, clearly labeled by status
6. Reusable AI workflow instruction
7. Five-case test plan and blank results table
8. Shared tool setup based on my organization’s existing tools
9. Roles, approvals, and maintenance path
10. Assumptions, gaps, conflicts, and the next three human actions

End with the smallest useful action I can take today. Do not propose expanding to another workflow until this one has been tested by someone other than its creator.
