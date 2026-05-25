# ConferenceAgent — Project Plan (10-Week Internship)

**Intern:** TBD
**Project Type:** Dossier Generator — pre-conference scientific intelligence report
**Timeline:** 10 weeks
**One-Sentence Description:** ConferenceAgent is an AI-powered scientific intelligence system that transforms conference abstracts and public signals into structured, source-grounded, pre-conference strategic reports.

---

## Project Goal

Develop an AI-powered agent that can automatically generate high-quality pre-conference intelligence reports from thousands of scientific abstracts, public announcements, clinical trial metadata, company disclosures, and social-media signals.

The system should help R&D, translational science, business development, competitive intelligence, and leadership teams quickly understand what matters before a major conference such as ASCO, AACR, ESMO, ASH, AHA, or AASLD.

## Core Problem

Before major scientific conferences, thousands of abstracts are released within a short time window. It is difficult for scientists and strategy teams to quickly answer:

- Which assets are most important?
- Which companies are gaining visibility?
- Which trials may change standard of care?
- Which technologies are emerging?
- Which signals are overhyped?
- Which assets are underappreciated?
- What should leadership track during and after the meeting?

ConferenceAgent automates the first-pass intelligence process.

---

## Expected Final Product

A working prototype that can generate a structured Markdown or Word report including:

1. Executive summary
2. Conference-level statistics
3. Top drugs, companies, and modalities
4. Cancer-type or disease-area summaries
5. Late-breaking abstract watchlist
6. Technology trend analysis
7. Company ranking
8. Social-media signal analysis
9. "Cognitive gap" / underappreciated asset section
10. Post-conference tracking checklist
11. Source table and data-quality disclaimer

---

## Key System Modules

### 1. Data Ingestion Module
Build a pipeline to ingest:
- Conference abstract exports
- LBA / oral / poster session files
- Drug and company dictionaries
- ClinicalTrials.gov metadata
- PubMed references
- Company press releases
- Social-media tracking files
- Manually curated expert notes

**Output:** a standardized master dataset.

### 2. Entity Extraction Module
Extract structured fields from abstracts:
- Drug name, target, company, disease area
- Trial phase, modality, biomarker, endpoint
- ORR, PFS, OS, HR, p-value
- Country / institution
- Presentation type

**Hybrid strategy:** rule-based dictionary matching · biomedical NER · LLM-assisted extraction · human-review flags for uncertain cases.

### 3. Modality Classification Module
Classify abstracts into technology themes:
- ADC, siRNA / RNA therapeutics, Gene therapy, Cell therapy
- T-cell engager, Bispecific antibody, ctDNA / MRD
- AI / ML, Small molecule, Immunotherapy
- Radioligand therapy, PROTAC / degrader, Biomarker / diagnostics

### 4. Quantitative Intelligence Dashboard
Generate summary tables:
- Total abstract count, top drugs / companies / targets / modalities
- Top disease areas, trial phase distribution
- LBA / oral / poster distribution
- Country or institution contribution
- Emerging themes

### 5. Social Signal Analysis Module
Analyze X / LinkedIn / public discussion signals if available:
- Most discussed assets, most active KOLs
- Peak engagement, duration of discussion
- Sentiment / narrative type
- Hype vs evidence mismatch

**Output:** "attention map" before the conference.

### 6. Report Generation Module
Use LLMs to generate a polished report from structured tables. Sections include what is hot, clinically important, underappreciated, what may change standard of care, which companies may benefit, and what to monitor after the conference.

**Important rule:** the LLM must not invent numbers. Every number must come from a source table.

### 7. Quality Control Module
Validation checks:
- All numerical claims trace back to source rows
- Drug-company mapping validated
- Trial phase verified
- LBA status verified
- Endpoint values checked
- Unsupported statements flagged
- Report includes data limitations

---

## 10-Week Plan

| Week | Milestone |
|------|-----------|
| 1 | Define use case, report template, and data schema |
| 2 | Build abstract ingestion pipeline |
| 3 | Build drug, company, disease, and modality dictionaries |
| 4 | Develop entity extraction workflow |
| 5 | Extract endpoints and clinical-trial metadata |
| 6 | Build quantitative summary tables |
| 7 | Add social-signal analysis module |
| 8 | Build LLM-based report generator |
| 9 | Add QC, source tracing, and hallucination checks |
| 10 | Generate final demo report and present prototype |

---

## Technical Stack

Python · pandas · spaCy / scispaCy · OpenAI API (or Gemini) · ClinicalTrials.gov API · PubMed API · Streamlit or Dash · Markdown / DOCX export · GitHub · optional LangChain or LlamaIndex.

## Final Deliverables

- Working Python pipeline
- Clean data schema
- Drug / company / modality dictionaries
- Example conference report
- Markdown and Word export function
- QC checklist
- Demo dashboard
- GitHub repository
- Final presentation

## Success Criteria

ConferenceAgent is successful if it can:
- Process 5,000–10,000 abstracts
- Extract major drugs, companies, diseases, and modalities
- Generate reliable summary tables
- Produce a readable pre-conference report
- Identify overhyped and underappreciated assets
- Reduce manual report preparation time by **≥ 70%**
- Provide traceable evidence for all key claims

## Stretch Goal

A reusable system that supports multiple conference types:
- ASCO / AACR / ESMO: oncology
- ASH: hematology
- AHA / ACC: cardiovascular
- AASLD / EASL: liver disease
- ADA: metabolic disease
- BIO / JPM: business development and investment intelligence

---

## Realistic CV Entry

*Built ConferenceAgent, an AI-orchestrated scientific intelligence system that ingests 5,000–10,000 conference abstracts plus ClinicalTrials.gov, PubMed, and social-signal data, extracts structured entities (drug, target, company, modality, endpoint), and generates a source-grounded pre-conference report — with QC enforcing zero invented numbers.*

- Engineered an ingestion + entity-extraction pipeline using rule-based dictionaries, biomedical NER, and LLM-assisted extraction.
- Built quantitative intelligence tables and an LLM report generator that draws **only** from structured source rows, enforced by a QC module.
- Delivered Markdown / DOCX export, demo dashboard, and a reusable framework extensible to multiple major medical and BD conferences.
