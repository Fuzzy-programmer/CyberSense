# CyberSense

A web app that helps non-technical users understand active cybersecurity
incidents — a browsable feed of current attacks and vulnerabilities explained
in plain English, with a chatbot to go deeper on any incident, grounded in
real cited sources.

## Why

Cybersecurity news and advisories are written for practitioners (CVE IDs,
CVSS scores, technical jargon). A non-technical person has no easy way to
know what an incident means for them, what to do about it, or even that it's
happening at all.

## Approach

- Pull data from two sources with different roles: live security news
  (discovery — what's happening now) and CISA's Known Exploited
  Vulnerabilities list (confirmed vulnerabilities with real mitigation paths)
- Normalize both into structured markdown incident records
- Use an LLM to generate a plain-language summary and protection steps per
  incident
- Serve a feed of incidents; each incident has its own scoped chat for
  follow-up questions, grounded only in that incident's source material
  (Retrieval-Augmented Generation)

## Status

🚧 Early build — ingestion from both sources in progress.

## Stack

Python, FastAPI, sentence-transformers, ChromaDB

---
*More detail on architecture and build steps to follow as the project takes shape.*
