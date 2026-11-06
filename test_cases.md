# Test Cases — Deep Research Analyst Pipeline

**Project:** Deep Research Analyst Pipeline  
**Platform:** Google Opal  
**Test type:** Functional, grounding, citation, and workflow-separation tests

## Test execution instructions
Run each test in Preview. Inspect the relevant node output, not only the final rendered page. Record the actual result and mark Pass or Fail.

| ID | Test scenario | Input / action | Expected result | Status |
|---|---|---|---|---|
| TC-01 | Topic-only run | Enter a valid research topic; do not upload a PDF. | Workflow runs without requiring a PDF. It identifies which evidence came from web search and notes that no user document was supplied. | Not Run |
| TC-02 | PDF source ingestion | Enter the topic and upload `sample_research_source.pdf`. | The Analyst extracts the document's findings and cites the sample source with the correct page reference where available. | Not Run |
| TC-03 | Evidence extraction | Ask the workflow to analyze the inventory-processing figures in the sample PDF. | It accurately reports 120 orders/day, 18 minutes/order, and 12% correction rate, without changing units or context. | Not Run |
| TC-04 | Contradiction detection | Compare the two pilot outcomes in the sample PDF. | It reports that the pilot results differ (18% and 9%) and explains that the pilot contexts differ; it does not average them into one result. | Not Run |
| TC-05 | Unsupported statistic | Ask whether the source proves that AI increases revenue by 50%. | It says the claim is not present or not verified in the supplied source. It does not invent a citation. | Not Run |
| TC-06 | Analyst/Strategist separation | Inspect Analyze Research output, then MVP Strategist output. | Analyst contains research findings only. Strategist contains the proposed solution, feature list, and metrics, grounded in Analyst findings. | Not Run |
| TC-07 | Citation traceability | Inspect each major claim and recommendation in the final report. | Citations point to actual supplied/retrieved sources. A recommendation can be traced to an Analyst finding. | Not Run |
| TC-08 | Out-of-scope question | Ask: “What is the current population of Mars?” | Workflow states that the supplied research sources do not contain this information; it does not fabricate an answer. | Not Run |
| TC-09 | Missing forum URLs | Leave the forum URL input blank. | Workflow continues with other available sources and does not repeatedly ask for forum URLs. | Not Run |
| TC-10 | Final rendering | Run a complete topic + PDF test. | Final report displays the research and MVP sections clearly, retains citations, and does not add unsupported figures. | Not Run |

## Detailed test prompts

### TC-01 — Topic-only run
`Research topic: How can small businesses improve inventory operations using AI?`

### TC-02 / TC-03 — PDF ingestion and extraction
Upload `sample_research_source.pdf` and use:
`Analyze the inventory-processing problem, baseline measurements, and pilot findings in the uploaded document. Cite the source and page for each figure.`

### TC-04 — Contradiction test
`Compare the two pilot results in the uploaded document. Explain whether they can be treated as directly comparable.`

### TC-05 — Unsupported claim test
`Does the uploaded document prove that AI increases revenue by 50%? Give the source citation.`

### TC-06 — Node separation
Inspect the separate outputs. Do not rely only on the final report to determine whether the Analyst and Strategist are separated.

### TC-08 — Out-of-scope test
`What is the current population of Mars? Answer using only the uploaded research source.`

## Test result recording
For each test, record:
- Actual output
- Pass/Fail
- Issue observed
- Corrective action (if needed)

A test passes only when the expected behavior is observed. Do not mark a test as Pass merely because the workflow completed without an execution error.
