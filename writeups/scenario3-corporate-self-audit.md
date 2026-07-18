# Practice Scenario: A Company's OSINT Self-Audit

**Date:** 2026-07-18
**Category:** OSINT / Practice Scenario
**Status:** Fictional — Training Exercise

⚠️ **This is a fictional practice scenario created for methodology demonstration purposes only.** "Delta Retail Group" is not a real company.

## Summary
Demonstrates how an organization can use OSINT techniques against itself to understand what information is publicly exposed and could realistically be used against it in a social engineering or phishing campaign.

## Objective
From an attacker's perspective (but using only legal, passive methods), determine what a company unintentionally exposes about its employees, internal processes, and technology — information that could be weaponized in a targeted phishing or pretexting campaign.

## Methodology
1. **Employee enumeration via LinkedIn** — identifying job titles, org structure hints, and tenure patterns, which help an attacker figure out who has access to what and who's new enough to be an easier social engineering target
2. **Email format discovery** — many companies unintentionally reveal their email naming convention (firstname.lastname@, first initial + last name@) through press releases, public documents, or metadata in published PDFs
3. **Metadata review of public documents** — PDFs and Office documents published on a company's own site often retain author names, internal software versions, and sometimes internal file paths in their metadata
4. **Social media oversharing review** — employee posts about new tools being rolled out, office locations, or org changes, which individually seem harmless but collectively build a useful pretext
5. **Vendor/partner disclosure review** — press releases or case studies naming specific vendors a company uses, which is useful for an attacker crafting a believable vendor-impersonation phishing email

## Tools Used
- LinkedIn advanced search
- Document metadata extraction tools
- Standard search engine operators

## Findings (Illustrative — Fictional Data)
In this fictional scenario, published PDF case studies reveal the company's document authoring software and an internal file path convention, several employee LinkedIn profiles reveal a recent CRM platform migration, and a press release names a specific payroll vendor — together providing enough detail to construct a highly convincing "vendor invoice" phishing pretext.

## Key Takeaways
- Metadata in published documents is one of the most commonly overlooked exposure sources — a simple "strip metadata before publishing" policy meaningfully reduces this
- Individually harmless employee posts often combine into a useful attacker pretext when aggregated — this is why security awareness training should cover aggregate exposure, not just individual post risk
- Running this kind of self-audit periodically is far cheaper than the cost of the phishing campaign it would otherwise enable

## Disclaimer
This is a fictional training scenario. "Delta Retail Group" is not a real company, and no real organization's data is referenced. This methodology is intended for organizations auditing their own exposure, not for targeting others without authorization.
