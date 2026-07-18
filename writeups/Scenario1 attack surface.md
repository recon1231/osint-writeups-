# Practice Scenario: Mapping a Company's External Attack Surface

**Date:** 2026-07-18
**Category:** OSINT / Practice Scenario
**Status:** Fictional — Training Exercise

⚠️ **This is a fictional practice scenario created for methodology demonstration purposes only.** "Northwind Logistics" is not a real company. No real organization, domain, or individual is referenced.

## Summary
A walkthrough of how to map a company's external attack surface using only passive, publicly available techniques — demonstrated against a fictional target company.

## Objective
Given only a company name ("Northwind Logistics") and its main domain, identify its externally-facing infrastructure footprint without any active scanning or unauthorized access.

## Methodology
1. **WHOIS/RDAP lookup** on the primary domain to identify registrar, registration date, and any exposed registrant details
2. **Certificate transparency search** (crt.sh) to enumerate subdomains that have ever had a TLS certificate issued — this often reveals staging, admin, or internal-tool subdomains never meant to be public
3. **DNS record review** (MX, TXT, NS records) to identify email providers, SPF/DMARC configuration, and hosting providers
4. **Job postings review** — job listings frequently reveal the internal tech stack (e.g., "experience with X ticketing system" or "familiarity with Y cloud platform") without the company realizing how much that discloses
5. **Public code repository search** — checking whether any employees have public repositories referencing company infrastructure, internal tool names, or (in real-world cases) accidentally committed credentials

## Tools Used
- WHOIS/RDAP
- crt.sh
- Standard DNS lookup tools
- Job board search

## Findings (Illustrative — Fictional Data)
For this fictional scenario, a hypothetical result might reveal: a staging subdomain (`staging.northwindlogistics.example`) discovered via certificate transparency that isn't linked anywhere on the main site, an outdated SPF record suggesting inconsistent email security configuration, and a job posting referencing a specific ticketing platform version.

## Key Takeaways
- Certificate transparency logs are one of the highest-value, lowest-effort passive recon sources — many organizations don't realize forgotten subdomains remain discoverable this way
- Job postings are an underrated OSINT source for technology stack fingerprinting
- None of this methodology requires touching the target's systems directly — attack surface mapping is almost entirely a passive-data exercise

## Disclaimer
This is a fictional training scenario. "Northwind Logistics" is not a real organization. All findings described are illustrative examples of what this methodology can reveal, not actual data from any real target.
