# Project Documentation Guidelines

## 1. Purpose and goals of documentation

### Why documentation exists
- Create a shared understanding across sales, product, design, and delivery.
- Preserve discovery context and decisions so work is consistent over time.
- Support clear customer-facing narratives without relying on individual memory.
- Provide traceability from inputs (notes) to outputs (narratives).

### What good documentation enables
- Faster alignment and fewer rework cycles.
- Consistent messaging across meetings, emails, and written materials.
- Clear ownership of assumptions, risks, and next steps.
- Confident handoffs between roles and phases of presales.

## 2. Documentation taxonomy (what goes where)

### README.md as the entrypoint
- Treat the repository README as the front door.
- It should link into the narrative and working materials using relative links.
- It should describe what is current, what is draft, and where to start.

### docs/narrative/ for customer-ready storytelling
- Use for polished, externally shareable narratives.
- Content should read as a cohesive story: context, problem, value, scope, assumptions, risks, timeline, pricing narrative, and FAQ.
- Keep it stable and deliberately edited.

### docs/working/ for internal notes and tracking
- Use for capture, collaboration, and execution tracking.
- This is where raw notes live and where action items are managed.
- Expect frequent edits and incremental updates.

### ai-rules/ for authoring rules and governance
- Use for documentation standards, constraints, and governance rules.
- These files define how the repository is written and maintained.
- Changes should be intentional and reviewed.

## 3. Folder-specific usage rules

### README.md
**What belongs here**
- The simplest starting point for a new contributor.
- Pointers to the current narrative and the most active working documents.
- A short explanation of how to navigate and where updates should go.

**What does NOT belong here**
- Meeting transcripts or long-form discovery notes.
- Detailed arguments, debate logs, or unresolved brainstorming.

**Tone and audience**
- Neutral, clear, and welcoming.
- Written for internal contributors first, but safe to share if needed.

### docs/narrative/
**What belongs here**
- Customer-ready content that represents the current story.
- Summarized findings, validated statements, and approved framing.
- Clear, decision-supporting language.

**What does NOT belong here**
- Raw meeting notes, transcripts, or unverified claims.
- Internal-only commentary about individuals, negotiation tactics, or sensitive internal process notes.
- Technical solution design, implementation plans, or architecture.

**Tone and audience**
- Professional and business-friendly.
- Written to be understandable by non-technical stakeholders.
- Prefer concrete statements; if uncertain, state the uncertainty explicitly.

### docs/working/
**What belongs here**
- Discovery notes and internal working material.
- Questions, action items, meeting notes, contacts, and progress tracking.
- Intermediate drafts that are not yet narrative-ready.

**What does NOT belong here**
- Final customer-facing narrative content once it is ready for external sharing.
- Technical implementation design details.

**Tone and audience**
- Internal and operational.
- Clear and factual, but can be more informal than narrative content.
- Capture intent and context, not polished prose.

### ai-rules/
**What belongs here**
- Documentation governance rules.
- Writing standards and constraints.
- AI usage rules for editing and summarization.

**What does NOT belong here**
- Project-specific discovery content or customer details.
- Any narrative content intended for external sharing.

**Tone and audience**
- Directive and consistent.
- Written for contributors who need to follow a common standard.

## 4. Authoring standards

### File naming conventions
- Keep existing structure and file names as the source of truth.
- Do not create new folders or relocate documents.
- If a file title needs to change, prefer updating the document title inside the file rather than renaming.

### Markdown structure and style
- Use one H1 at the top of each document.
- Use clear section headers (##, ###) and short sections.
- Prefer bullet lists over long paragraphs.
- Use plain language and avoid unnecessary jargon.
- Use consistent lists and consistent capitalization for repeated headings.

### Voice and audience guidance
- docs/narrative/: confident, business-first, externally safe.
- docs/working/: practical, internal, capture-focused.
- Avoid sales hype and absolute claims unless validated.
- When information is missing or not validated, state it directly.

### Terminology consistency rules
- Use one term per concept and keep it consistent across documents.
- Define acronyms on first use within each document.
- Use the same names for stakeholders, teams, and artifacts throughout the repository.
- When a term changes, update narrative first, then align working notes as needed.

## 5. Required content patterns

### Decisions (what to record and where)
- Record decisions in the most relevant working document where the decision was made or captured.
- Each decision entry should include:
	- Decision statement (one sentence)
	- Date (if known)
	- Owner (who confirmed it)
	- Rationale (short)
	- Impact (what changes because of it)
	- Links to affected narrative sections

### Assumptions (ownership, validation, linkage to risks)
- Capture assumptions explicitly when facts are unknown.
- Each assumption should include:
	- Assumption statement
	- Owner (who is responsible for validating)
	- Validation plan (how it will be confirmed)
	- Status (unvalidated, in progress, validated, invalidated)
	- Link to related risks and narrative sections

### Risks and dependencies (structure and ownership)
- Track risks and dependencies with clear ownership.
- Each item should include:
	- Description
	- Type (risk or dependency)
	- Owner
	- Likelihood and impact (simple scale is fine)
	- Mitigation or next step
	- Link to assumptions and narrative sections affected

### Action items (ownership, status, location)
- Action items live in working documents where tracking is already established.
- Every action item must include:
	- Owner
	- Due date or target timeframe (if known)
	- Status (not started, in progress, blocked, done)
	- A link to the context that created it

## 6. Update workflow

### Capture vs synthesize
- Capture belongs in docs/working/.
- Synthesis belongs in docs/narrative/.
- Do not paste raw notes into narrative documents.

### Change traceability
- When updating narrative content, ensure the supporting working notes exist.
- Prefer adding a short note in the relevant working file that explains what changed and why.
- Keep statements attributable to a source (meeting, workshop, stakeholder confirmation) when possible.

### Narrative consistency checks
- Maintain alignment across narrative sections (problem, value, use cases, scope).
- If a narrative change affects assumptions, risks, timeline, or pricing narrative, update those sections as part of the same edit.
- Avoid contradictory statements across narrative chapters.

### Deprecation rules (do not delete silently)
- Do not delete content without leaving a trace.
- When something is outdated:
	- Mark it clearly as deprecated
	- Explain what replaced it
	- Link to the new source of truth
- Prefer editing forward rather than erasing prior context.

## 7. Reviews and ownership

### Ownership model
- Each document should have a clear owner responsible for keeping it current.
- Ownership is role-based, not person-based, where possible.
- Owners are responsible for resolving conflicts in messaging and content.

### Review triggers
- Review narrative documents before any external sharing.
- Review after major discovery events (workshops, stakeholder interviews) that change:
	- Problem statement
	- Value proposition
	- Scope
	- Assumptions
	- Risks
	- Timeline
	- Pricing narrative

### Suggested update cadence
- Working notes: update continuously during active presales periods.
- Narrative documents: update after meaningful changes, not daily.
- Governance rules (ai-rules/): review when process issues appear or when contributors change.

## 8. Linking, navigation, and diagrams

### README linking expectations
- README should link to:
	- Narrative overview and the primary narrative flow
	- The current working agenda and next steps
	- Where questions, risks, and assumptions are tracked

### Relative links
- Use relative links between documents.
- Prefer linking to the most stable document rather than transient notes.
- Avoid broken links by keeping referenced filenames stable.

### Diagram placement and referencing rules
- Diagrams live where the repository already defines them.
- Reference diagrams from narrative content only when they improve clarity.
- Each diagram reference should include a one-line explanation of what the diagram shows and why it matters.

## 9. Quality checklist

Use this checklist before sharing any narrative content externally:
- No unverified facts presented as truth.
- No internal-only commentary (people, negotiations, internal process).
- Problem, value, scope, assumptions, and risks are consistent across narrative chapters.
- Claims are specific, measurable where possible, and not exaggerated.
- All acronyms are defined on first use.
- Links work and point to the correct source of truth.
- Sensitive information is removed or generalized.

## 10. AI-assisted editing guidance

### What AI is allowed to do
- Improve clarity, grammar, and structure without changing meaning.
- Summarize working notes into draft narrative language, clearly marked as draft.
- Normalize formatting and headings to match standards.
- Identify inconsistencies, missing sections, and unclear statements.

### What AI must never invent
- Customer names, metrics, quotes, dates, commitments, or outcomes.
- Product capabilities, technical approaches, or implementation designs.
- Pricing details, contractual terms, or delivery promises.
- Decisions, approvals, or stakeholder intent that is not documented.

### Verification expectations
- All AI-generated factual statements must be verified against existing working notes.
- If verification is not possible, the content must be written as an open question or explicit assumption.
- External sharing requires human review of narrative documents.
