# PubChem

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

PubChem is NCBI's open chemistry database containing information on more than 100 million chemical compounds. Operated by the National Center for Biotechnology Information (NCBI) at the U.S. National Institutes of Health (NIH), PubChem provides free programmatic access to chemical structures, molecular properties, bioactivity data, safety information, and drug information through REST and SOAP APIs.

## APIs

### PUG REST API
The Power User Gateway (PUG) REST API is the primary interface for programmatic access to PubChem data. It supports lookup of compounds by name, CID, SMILES, InChI, and structure search. Key operations include:

- Compound property retrieval (molecular formula, weight, logP, TPSA, etc.)
- Structure search (substructure, superstructure, similarity)
- Bioassay result summaries
- Cross-reference lookups (CAS, ChEMBL, ChEBI, etc.)
- 2D structure image generation

Base URL: `https://pubchem.ncbi.nlm.nih.gov/rest/pug`

Documentation: https://pubchem.ncbi.nlm.nih.gov/docs/pug-rest

### PUG View API
The PUG View API returns the full structured data pages for compounds and substances, organized hierarchically as displayed on the PubChem website. Covers names, identifiers, structures, physical and chemical properties, safety data, pharmacology, toxicology, biological activities, and literature.

Base URL: `https://pubchem.ncbi.nlm.nih.gov/rest/pug_view`

Documentation: https://pubchem.ncbi.nlm.nih.gov/docs/pug-view

### PUG SOAP API (Legacy)
Legacy SOAP/XML interface supporting structure search, identity search, and chemical standardization. New integrations should use the REST API.

WSDL: https://pubchem.ncbi.nlm.nih.gov/pug/pugsoap.cgi?wsdl

### Structure Image Service
Generates 2D structure images in PNG format for compounds identified by CID, name, or SMILES.

### Identifier Exchange Service
Bulk identifier conversion between PubChem CIDs, SIDs, and external identifiers including CAS Registry Numbers, ChEMBL, and ChEBI.

Service URL: https://pubchem.ncbi.nlm.nih.gov/idexchange/idexchange.cgi

## Authentication

PubChem APIs are free and publicly accessible without authentication. For higher rate limits, register a free NCBI API key at https://www.ncbi.nlm.nih.gov/account/ and pass it as the `api_key` query parameter.

## Rate Limits

| Access Type | Rate Limit |
|---|---|
| Anonymous | 5 requests/second per IP |
| NCBI API Key | 10 requests/second |

For bulk data needs exceeding these limits, use FTP downloads at https://ftp.ncbi.nlm.nih.gov/pubchem/

## Cost

PubChem is a free U.S. government service funded by NIH. There are no costs, subscription fees, or usage-based charges for any API or data service.

## Links

- Website: https://pubchem.ncbi.nlm.nih.gov/
- Documentation: https://pubchem.ncbi.nlm.nih.gov/docs/
- Blog: https://pubchemblog.wordpress.com/
- FTP Bulk Data: https://ftp.ncbi.nlm.nih.gov/pubchem/
- Support: https://support.nlm.nih.gov/
- NCBI Account (API Key): https://www.ncbi.nlm.nih.gov/account/
