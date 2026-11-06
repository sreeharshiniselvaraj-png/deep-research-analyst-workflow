# Workflow Documentation

## 1. Objective
Build a grounded research workflow in Google Opal that turns a research topic and available source material into an evidence-based analysis and a traceable MVP proposal.

## 2. Workflow stages

### Stage 1 — User input and source ingestion
**Inputs**
- Research topic (required)
- Uploaded PDF documents (optional)
- Forum URLs (optional)
- Video transcripts (optional)

**Expected behavior**
- Accept a topic even when no PDF is uploaded.
- Process only sources that are actually supplied or retrieved.
- Clearly report missing, inaccessible, or empty source inputs.

### Stage 2 — Search and retrieval
**Purpose**
Find relevant public sources where web search is configured. Retrieve forum pages only when URLs are supplied.

**Expected output**
- Source title and publisher
- Publication date, when available
- Direct URL
- Relevant evidence or passage
- Retrieval/access limitations

### Stage 3 — Analyze Research
**Purpose**
Produce research analysis only. Do not propose a product or MVP.

**Required analysis**
- Research topic and scope
- Available sources
- Key themes and patterns
- User needs and pain points
- Emerging trends
- Cross-source comparison
- Supporting evidence and statistical verification
- Research gaps and limitations
- Summary of key findings
- References

**Evidence rules**
- Preserve source context, population, geography, date, and measurement.
- Distinguish general AI usage, pilots, operational deployment, and scaled integration.
- Do not combine unrelated statistics.
- Mark claims Verified, Partially Verified, or Unverified.
- Never invent citations or page numbers.

### Stage 4 — MVP Strategist
**Purpose**
Generate a practical MVP proposal using only the Analyst output.

**Expected sections**
- Core problem
- Target users
- Proposed MVP solution
- Essential features
- Feature prioritization
- Expected business value
- Risks and limitations
- Success metrics
- High-level implementation outline
- Evidence traceability and missing information

Recommendations must point back to Analyst findings. Proposed outcomes must be labelled as hypotheses or targets, not achieved results.

### Stage 5 — Final report rendering
Combine the Analyst report and MVP strategy into a readable final report. Preserve citations and uncertainty labels. Do not add new unsupported claims.

## 3. Completion criteria
The workflow is successful when:
- The topic flows through all required nodes.
- The Analyst produces research-only findings.
- The Strategist produces a separate evidence-grounded MVP proposal.
- The final report preserves citations and limitations.
- Unsupported and out-of-scope questions are handled honestly.
