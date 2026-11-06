# Deep Research Analyst Pipeline (Topic 8)

A Google Opal workflow that follows **Search → Analyst → Strategist → Final Report**.

## Project purpose
This project demonstrates a research workflow that:
1. Accepts a research topic and optional source material.
2. Collects evidence from available sources.
3. Analyzes findings, patterns, contradictions, and evidence gaps.
4. Generates an MVP proposal based only on the Analyst output.
5. Renders a final report with traceable citations.

## Workflow
```text
Research Topic + Optional Documents / URLs / Transcripts
                         |
                  Search / Retrieval
                         |
                  Analyze Research
                         |
                   MVP Strategist
                         |
                Render Research Report
```

## Repository contents
- `workflow_documentation.md` — workflow purpose, nodes, inputs, and outputs.
- `test_cases.md` — functional and quality test cases.
- `sample_research_input.md` — source text used for manual/prompt testing.
- `expected_test_results.md` — expected behavior and pass criteria.
- `evidence_and_citation_rules.md` — source-grounding rules.
- `sample_research_source.pdf` — synthetic test fixture for testing PDF upload and citation extraction.

## Important note about the sample PDF
The PDF is **synthetic test data**. Its example figures and organizations are fictional and must not be presented as real-world facts. It is designed only to test whether the workflow extracts, cites, separates, and refuses unsupported information correctly.

## How to test in Google Opal
1. Open the Deep Research Analyst Pipeline.
2. Enter the topic: `How can small businesses improve inventory operations using AI?`
3. Upload `sample_research_source.pdf`.
4. Run the workflow.
5. Inspect the Analyst output, Strategist output, and final rendered report separately.
6. Execute the test cases in `test_cases.md`.
7. Record actual results and update the status column.

## Suggested GitHub upload
Upload all files in this folder to the root of your GitHub repository. Keep the sample PDF in the repository so reviewers can reproduce the upload test.
