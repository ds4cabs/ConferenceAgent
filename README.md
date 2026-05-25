# ConferenceAgent

[![CABS: ds4cabs](https://img.shields.io/badge/CABS-ds4cabs-1f4b99?logo=github)](https://github.com/ds4cabs)
[![GitHub Pages: live](https://img.shields.io/badge/GitHub_Pages-live-brightgreen?logo=github)](https://ds4cabs.github.io/ConferenceAgent/)
![CABS: 2026](https://img.shields.io/badge/CABS-2026-6f42c1)
![status: MVP in progress](https://img.shields.io/badge/status-MVP_in_progress-f1c40f)
![type: Dossier Generator](https://img.shields.io/badge/type-Dossier_Generator-1f6feb)
![domain: Scientific Conference Intelligence](https://img.shields.io/badge/domain-Scientific_Conference_Intelligence-0aa)

**Intern:** TBD
**Project Type:** Dossier Generator (LLM-orchestrated, source-grounded report)

## Overview
ConferenceAgent is an AI-powered scientific intelligence system that transforms thousands of conference abstracts, public announcements, ClinicalTrials.gov metadata, company disclosures, and social-media signals into a structured, source-grounded, pre-conference strategic report for major meetings such as ASCO, AACR, ESMO, ASH, AHA, and AASLD.

## Deliverable
- Python pipeline that ingests abstracts + structured external sources
- Drug / company / disease / modality dictionaries
- Entity-extraction and modality-classification workflow
- Quantitative summary tables (top drugs, companies, modalities, LBAs)
- LLM-based Markdown / DOCX report generator with citation provenance
- QC module enforcing "no invented numbers" and traceable claims

## Core Tools
- ClinicalTrials.gov API
- PubMed E-utilities
- Conference abstract exports (ASCO / AACR / ESMO / ASH)
- Company press-release feeds
- X / LinkedIn public-signal exports
- Open Targets, ChEMBL (drug-target / modality enrichment)
- Manually curated expert-note files

## Tech Stack
Python, pandas, spaCy / scispaCy, OpenAI / Gemini API, Streamlit or Dash, markdown-pdf / `python-docx`, optional LangChain / LlamaIndex.

## Notes
The agent must never invent numbers. Every quantitative claim in the final report must trace back to a source row in the structured tables. QC is a first-class module, not an afterthought.
