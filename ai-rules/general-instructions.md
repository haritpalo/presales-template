# General Instructions

## Purpose
These instructions exist to keep presales and discovery documentation consistent, accurate, and decision-ready. They prevent guessing, scope creep, and contradictory narratives across documents. AI is a writing and organizing assistant. It supports human judgment and does not replace it.

## Non-negotiable rules
- Review before writing: read the relevant existing documents before drafting or editing.
- No guessing: do not invent company names, metrics, timelines, decisions, stakeholders, constraints, pricing, or commitments.
- Flag missing information: explicitly mark gaps and ask targeted questions instead of filling them.
- Follow the fixed structure: do not create, rename, remove, or suggest new files or folders.
- Preserve intent: do not change meaning, commitments, or positioning unless explicitly instructed.
- Avoid scope creep: do not broaden scope, add new initiatives, or introduce new workstreams.
- Business-only content: keep language suitable for non-technical and mixed audiences.
- Implementation or solution design: provide only on demand (only when explicitly requested), and never by default.
- Feature or solution recommendations: provide only on demand (only when explicitly requested), and never by default.
- Respect uncertainty: clearly label what is confirmed versus unconfirmed.

## Default working style

### How AI gathers context before writing
- Identify the target document and its purpose (narrative, working, or AI rules).
- Scan for the latest statements of:
  - Business context and objectives
  - Problem statement and impact
  - Use cases and success criteria
  - Scope and exclusions
  - Assumptions, risks, dependencies
  - Timeline and milestones
  - Pricing narrative and constraints
- Reuse existing phrasing when possible to avoid drift.
- If sources conflict, surface the conflict and ask which version is correct.

### When AI must ask clarifying questions
- When a statement would introduce a new commitment, decision, date, cost driver, or scope boundary.
- When the document would otherwise rely on implied context.
- When required sections are empty and cannot be grounded in existing notes.
- When there are contradictions across documents.

### When AI should propose an outline before drafting
- When creating a new version of a narrative section from scattered notes.
- When reorganizing content across multiple sections.
- When the requested change could affect scope, timeline, pricing narrative, risks, or assumptions.
- When the audience is external (client-facing) and the story flow matters.

## Writing tone and rules by folder

### docs/narrative
- Audience: client-facing and executive.
- Tone: confident, neutral, and business-oriented.
- Style: linear story, minimal repetition, clear decisions and boundaries.
- Avoid: internal debate, speculation, casual language, and open-ended brainstorming.

### docs/working
- Audience: internal presales team and cross-functional partners.
- Tone: factual, concise, and action-oriented.
- Style: bullets, short sections, clear owners, and clear follow-ups.
- Allow: open questions, unknowns, and rough notes when labeled.

### ai-rules
- Audience: repository maintainers and contributors.
- Tone: directive and precise.
- Style: rules, workflows, checklists.
- Avoid: project-specific content and client-specific claims.

## Intent preservation and scope control

### Preserving intent
- Keep original meaning and emphasis.
- Do not change commercial posture, inclusions, exclusions, or risk framing unless explicitly requested.
- If a requested change could alter intent, pause and confirm the desired intent in one or two questions.

### Avoiding scope creep
- Only address what is requested.
- Do not introduce new categories of work, new stakeholders, or new outcomes.
- If the user asks for new content outside the fixed documents, explain it is out of scope and offer to place it in the appropriate existing file.

## Placeholders and explicit status labeling
Use explicit placeholders when information is missing or pending.

Required placeholder patterns:
- `TBD:` for content that must be drafted later.
- `To confirm:` for facts requiring validation.
- `Owner:` for responsibility.
- `Due date:` for deadlines.
- `Decision needed:` when a choice is required.

Rules:
- Do not leave ambiguity unmarked.
- Do not convert placeholders into facts without an explicit source.

## Traceability and grounding

### Grounding expectations
- Prefer statements grounded in the existing repository content.
- If a claim is not grounded, label it as `To confirm:` and ask for the source.

### Handling uncertainty
- Use clear qualifiers only when necessary: `Confirmed:`, `Assumed:`, `Unconfirmed:`.
- If the user requests certainty that cannot be supported, explain what is missing and what would make it confirmable.

### Referencing sources
- When summarizing, reference the source document by file path and section name (without quoting line numbers).
- If multiple notes exist, state which note you used and the date if available.

## Scannability and formatting rules
- Use clear headers and short sections.
- Prefer bullet lists over long paragraphs.
- Keep bullets parallel and action-oriented.
- Use tables only when they improve clarity (for example, risks, assumptions, decisions).
- Keep tables small and readable.
- Use consistent terminology across documents.
- Avoid en dashes.

## Workflows

### Workflow: Updating narrative documents
1. Review the relevant narrative files in order to preserve the story flow.
2. Identify the change type:
	- Clarification (wording only)
	- Scope boundary (included or excluded)
	- Risk or dependency update
	- Timeline or milestone update
	- Pricing narrative adjustment
3. Locate where the change belongs. Do not duplicate content across chapters.
4. Draft the smallest change that achieves the request.
5. Check for downstream impact across:
	- 02 problem statement
	- 03 value proposition
	- 05 scope
	- 06 assumptions
	- 07 risks and dependencies
	- 08 timeline
	- 09 pricing narrative
6. If impact exists, propose aligned edits and ask for confirmation before applying.

### Workflow: Managing open questions
1. Capture questions in the questions log using one line per question.
2. Each question must include:
	- The question
	- `Owner:`
	- `Due date:`
	- `Context:` which document or decision it affects
3. When an answer arrives:
	- Move it to the answered section
	- Record the date and the source
	- Update the impacted narrative sections only if explicitly confirmed

### Workflow: Capturing meeting notes
1. Record meeting details (date, attendees, purpose).
2. Write notes as short bullets.
3. Separate:
	- Facts heard
	- Decisions made
	- Actions and owners
	- Open questions
4. Do not convert discussion into commitments unless explicitly stated as a decision.

### Workflow: Defining scope
1. Start from the stated problem and intended outcomes.
2. Write scope as two lists:
	- Included
	- Excluded
3. Add decision boundaries:
	- What is explicitly not being decided here
	- What requires client confirmation
4. If scope is vague, ask for:
	- Which use cases are priority
	- Which outcomes matter most
	- What must be excluded to keep focus

### Workflow: Managing risks and dependencies
1. List risks with:
	- Description
	- Business impact
	- Likelihood (if provided, otherwise `To confirm:`)
	- Mitigation as a business action
	- `Owner:` and `Due date:` where applicable
2. List dependencies with:
	- What is needed
	- Who provides it
	- When it is needed
3. Keep risks and dependencies aligned with scope and timeline.

## Quality checklist (run before completing work)
- I reviewed the relevant existing documents before drafting.
- I did not invent names, numbers, timelines, or decisions.
- I flagged missing information with `TBD:` or `To confirm:`.
- I preserved intent and did not change commitments.
- I avoided scope creep and stayed within the fixed structure.
- I used the correct tone for the target folder.
- The content is scannable with clear headings and bullets.
- Any updates that impact scope, timeline, pricing narrative, assumptions, or risks are consistent across documents.

## Interaction contract

### When AI should proceed
- The request is clearly scoped to existing files.
- The needed facts are present in the repository or the user provided them explicitly.
- The change is wording, organization, or summarization without adding new commitments.

### When AI must pause and ask questions
- Information is missing or contradictory.
- The request implies a decision, commitment, date, or pricing element not documented.
- The request would change scope boundaries, assumptions, risks, dependencies, timeline, or pricing narrative.

### How AI should respond to out-of-scope requests
- State that the request is out of scope for this repository.
- Offer a compliant alternative limited to:
  - Summarizing existing content
  - Flagging missing information
  - Drafting business-only text within the fixed documents
