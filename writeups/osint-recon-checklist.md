# My OSINT Recon Checklist — Where I Start Every Investigation

**Date:** 2026-07-18
**Category:** OSINT / Methodology
**Status:** Public

## Summary
A breakdown of the recon framework I use at the start of any OSINT investigation — the order I work in, the categories I always check, and why structure matters more than any single tool.

## Objective
New OSINT practitioners often jump straight to tools without a repeatable process, which means important angles get missed. This is the checklist I follow to make sure recon is thorough and consistent every time, regardless of the target type (person, domain, organization, or username).

## Methodology

**1. Define the objective before touching a single tool**
What exactly am I trying to find out? A vague goal ("learn about this domain") leads to unfocused research. A specific goal ("identify the hosting provider and any linked subdomains") keeps the investigation efficient.

**2. Passive recon first, always**
Before anything that could alert a target, gather everything available through passive means:
- WHOIS / historical WHOIS records
- DNS records and subdomain enumeration
- Cached versions of pages (Wayback Machine)
- Public breach/leak databases (for validating exposure, not for accessing stolen data)

**3. Username and identity correlation**
If working from a username or handle:
- Check consistent usage across platforms (same handle reused = high-confidence link)
- Look for reused profile photos (reverse image search)
- Cross-reference bios, writing style, and posting patterns for correlation, not just handle matches alone

**4. Infrastructure mapping (for domains/organizations)**
- Identify hosting provider, ASN, and IP ranges
- Map subdomains and any exposed services
- Check certificate transparency logs for related domains

**5. Social and public footprint**
- Public social media presence
- Public code repositories (GitHub, GitLab) — often leak more than people realize (API keys, internal tool names, employee usernames)
- Job postings — surprisingly rich source of internal tech stack and org structure info

**6. Timeline building**
Lay every piece of information found on a timeline. Patterns and inconsistencies often only become visible once data is chronological rather than scattered across notes.

**7. Verification pass**
Before treating anything as confirmed: can this be corroborated by a second, independent source? Single-source claims get flagged as "unconfirmed," not presented as fact.

## Tools Used
- **WHOIS/RDAP lookups** — ownership and registration history
- **crt.sh** — certificate transparency search for subdomain discovery
- **Wayback Machine** — historical page snapshots
- **Reverse image search (multiple engines)** — photo correlation across platforms
- **Maltego / manual link-mapping** — visualizing relationships between data points

## Key Takeaways
- A repeatable checklist beats "tool-hopping" — most missed findings come from skipped steps, not bad tools
- Passive-before-active isn't just an OPSEC habit, it also produces cleaner, less biased initial data
- Single-source information should always be labeled as unconfirmed until corroborated

## Disclaimer
This writeup describes general OSINT methodology only and does not reference any specific real target, investigation, or client. No real target, victim, or client data is included.
